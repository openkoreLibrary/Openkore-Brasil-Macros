
# 📦 Biblioteca de Macros para OpenKore

Uma coleção de macros úceis para automatizar ações no [OpenKore](https://openkore.com/).

## ✨ Funcionalidades

- Macros de suporte (buffs, healing, warp, etc.)
- Macros de farm e movimentação
- Auto venda e reabastecimento
- Resposta automática a mensagens
- Integrações com eventos e reações

> Todas as macros são compatíveis com o sistema de `macro.txt` do plugin [Macro Plugin](https://openkore.com/index.php/Macro_plugin).

---

## 📁 Estrutura do Projeto

```
macros/
├── buffs.txt         # Macros para buffs automáticos
├── farm.txt          # Caminhos e ações de farm
├── suporte.txt       # Macros para suportes (heal, warp, etc.)
├── npc-interact.txt  # Exemplos de interação com NPCs
├── utilidades.txt    # Diversas automações úceis
└── README.md
```

---

## 🛠️ Requisitos

- OpenKore com o plugin `macro.pl` instalado  
- Perl configurado corretamente  
- Conhecimento básico em configuração de bots no OpenKore

---

## 🚀 Como usar

1. Copie os arquivos `.txt` desejados para a pasta `control/macros` do seu OpenKore.
2. No `config.txt`, ative o plugin macro:

   ```
   macroAuto 1
   ```

3. (Opcional) Edite os arquivos de macro conforme sua necessidade.
4. Inicie o OpenKore normalmente.

---

## 📚 Exemplos

### Buff automático a cada 60 segundos:

```perl
automacro auto_buff {
   spell_timeout Blessing > 55000
   class Monk
   run-once 0
   call {
      do ss 28 <me>
      do conf spell_timeout_Blessing 60000
   }
}
```

### Caminho de farm simples:

```perl
macro farm_path {
   do move 125 200
   do move 130 195
   do move 135 190
   do move 140 185
}
```

---

## 🤝 Como contribuir

Contribuir é fácil! Se você tem ideias novas, melhorias ou correções, siga os passos abaixo:

1. **Fork** este repositório.
2. **Crie uma branch** nova para sua contribuição:
   ```
   git checkout -b minha-nova-macro
   ```
3. **Adicione suas macros ou alterações** com boas descrições e comentários se necessário.
4. **Faça um commit** claro:
   ```
   git commit -m "Adiciona macro para auto venda no NPC"
   ```
5. **Envie para seu fork** e abra um **Pull Request**.

Se você não manja de Git, pode só abrir uma [Issue](https://github.com/seu-usuario/seu-repo/issues) descrevendo a sugestão ou mandar um `.txt` da macro que a gente adiciona!

---

## 🧙‍♂️ Créditos

Feito por entusiastas do Ragnarok e do OpenKore.  
Junte-se a nós!
