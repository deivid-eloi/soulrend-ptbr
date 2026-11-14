# Soulrend PT-BR

Tradução não oficial para português do Brasil do modpack **Soulrend - Dark Fantasy RPG Soulslike** (v8.5.2, Forge 1.20.1).

Traduz itens, armas, feitiços, classes e raças, a tela de personagem, as missões do FTB Quests, o minimapa e o mapa-múndi, entre outros. Nomes próprios de armas e chefes ficam em inglês; nomes comuns são traduzidos.

## Downloads

| Download | O que é |
|---|---|
| [Baixar tradução dos jogadores](https://github.com/deivid-eloi/soulrend-ptbr/raw/refs/heads/main/dist/Soulrend-PTBR.zip) | Resource pack com os textos e livros traduzidos. |
| [Baixar tradução do servidor](https://github.com/deivid-eloi/soulrend-ptbr/raw/refs/heads/main/dist/Soulrend-PTBR-Servidor.zip) | Missões do FTB Quests + datapack independente de textos de classes e origens. |
| [Baixar somente o datapack](https://github.com/deivid-eloi/soulrend-ptbr/raw/refs/heads/main/dist/Soulrend-PTBR-Datapack.zip) | Para quem já instalou as missões traduzidas. |

Os arquivos são para **Soulrend v8.5.2**. O novo formato de datapack foi verificado estruturalmente, mas ainda precisa de validação dentro do jogo.

## Instalação no servidor

1. **Pare o servidor** e faça backup de `config/ftbquests/quests` e `config/paxi/datapacks`.
2. Baixe a tradução do servidor e extraia o ZIP na **raiz** do servidor, onde fica o `server.properties`. Mescle as pastas `config` existentes e aceite substituir somente os arquivos de quests com o mesmo nome. **Não apague nem substitua pastas inteiras.** O resultado inclui:
   - `config/ftbquests/quests/`: missões traduzidas.
   - `config/paxi/datapacks/Soulrend-PTBR-Datapack.zip`: tradução adicional de classes e origens. Deixe este ZIP fechado, ao lado das pastas dos datapacks originais.
3. No `server.properties`, deixe o resource pack **vazio**:
   ```properties
   resource-pack=
   resource-pack-sha1=
   ```
   Não envie a tradução pelo servidor. O jogo recarrega todos os packs quando recebe o pack do servidor; se a tela de escolha de raça estiver aberta nesse momento (primeiro login), o cliente crasha com `zip file closed` (otimização de idiomas do ModernFix). Cada jogador instala o pack manualmente (veja abaixo).
4. Ligue o servidor.

O Paxi carrega o datapack adicional automaticamente. Ele mantém os mesmos IDs, poderes e condições dos arquivos de referência e altera os textos e a prioridade de carregamento do Origins. Não é necessário substituir os arquivos dentro de `soulrend_origins_classes`. Consulte a [documentação do Paxi](https://www.curseforge.com/minecraft/mc-mods/paxi) e as prioridades de [origens](https://origins.readthedocs.io/en/latest/json/origin/) e [camadas](https://origins.readthedocs.io/en/latest/json/origin_layer/).

### Já instalou as quests traduzidas?

Baixe **somente o datapack**, coloque o ZIP em `config/paxi/datapacks/` e reinicie o servidor. Confira com `/datapack list enabled` se ele aparece e verifique os textos de classes e origens no jogo.

Se já mesclou os arquivos antigos do Paxi, pode adicionar o novo ZIP sem restaurá-los. Se apagou a pasta inteira de um datapack original, restaure primeiro a pasta completa a partir do modpack **v8.5.2** e depois adicione o ZIP da tradução.

### Por que a pasta antiga parecia incompleta?

`dist/servidor/` contém apenas os arquivos que receberam tradução: 7 JSONs de um datapack e 62 arquivos de quests. É uma atualização parcial, destinada a ser **mesclada** com os originais; não é uma cópia completa do Paxi. Os demais datapacks e arquivos continuam sendo necessários. Essa pasta permanece disponível como formato antigo; os downloads acima usam o novo datapack independente.

As missões desta versão são traduzidas diretamente nos arquivos de configuração do FTB Quests; o resource pack dos jogadores e o datapack adicional não substituem essa etapa. Atualizações do modpack exigem revisar e gerar novamente os arquivos de servidor, pois o datapack traduzido contém definições da versão 8.5.2.

## Para os jogadores

1. Baixe a [tradução dos jogadores](https://github.com/deivid-eloi/soulrend-ptbr/raw/refs/heads/main/dist/Soulrend-PTBR.zip) (`Soulrend-PTBR.zip`).
2. No CurseForge, clique com o botão direito no modpack → **Abrir pasta** e coloque o ZIP (sem extrair) dentro de `resourcepacks`.
3. No jogo, em **Opções → Pacotes de recursos**, ative `Soulrend-PTBR.zip` e deixe-o **no topo** da lista.
4. Em **Opções → Idioma**, escolha **Português (Brasil)**.

Faça isso antes de entrar no servidor pela primeira vez, para a tela de escolha de raça já abrir traduzida. Quando sair uma versão nova da tradução, baixe o ZIP de novo e substitua o antigo.

## Aviso

Projeto de fã, sem vínculo com os autores do modpack ou dos mods. Os textos originais pertencem aos respectivos autores; este repositório contém só a tradução. Se você é autor de algum conteúdo e quer que ele seja removido, abra uma issue.
