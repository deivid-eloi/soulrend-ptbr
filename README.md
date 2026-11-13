# Soulrend PT-BR

Tradução não oficial para português do Brasil do modpack **Soulrend - Dark Fantasy RPG Soulslike** (v8.5.2, Forge 1.20.1).

Traduz itens, armas, feitiços, classes e raças, a tela de personagem, as missões do FTB Quests, o minimapa e o mapa-múndi, entre outros. Nomes próprios de armas e chefes ficam em inglês; nomes comuns são traduzidos.

## Conteúdo

| Arquivo | O que é |
|---|---|
| `dist/Soulrend-PTBR.zip` | Resource pack com os textos traduzidos (vai para os jogadores) |
| `dist/servidor/` | Missões e textos de datapack traduzidos (vão para o servidor) |

## Instalação no servidor

1. **Pare o servidor** e faça backup de `config/ftbquests/quests` e `config/paxi/datapacks`.
2. Copie o conteúdo de `dist/servidor/` para a **raiz** do servidor, substituindo os arquivos.
3. No `server.properties`:
   ```properties
   resource-pack=https://github.com/deivid-eloi/soulrend-ptbr/raw/main/dist/Soulrend-PTBR.zip
   resource-pack-sha1=bd1f24c970431e213c662ae83e0657f658775b63
   require-resource-pack=false
   resource-pack-prompt=Tradução PT-BR do modpack
   ```
   O SHA1 muda a cada versão do pack. Para calcular: `certutil -hashfile Soulrend-PTBR.zip SHA1` (Windows) ou `sha1sum Soulrend-PTBR.zip` (Linux).
4. Ligue o servidor.

## Para os jogadores

1. Em **Opções → Idioma**, escolha **Português (Brasil)**.
2. Ao entrar no servidor, aceite o pacote de recursos.

Para jogar sozinho, coloque `Soulrend-PTBR.zip` na pasta `resourcepacks` da instância e ative o pack no topo da lista.

## Aviso

Projeto de fã, sem vínculo com os autores do modpack ou dos mods. Os textos originais pertencem aos respectivos autores; este repositório contém só a tradução. Se você é autor de algum conteúdo e quer que ele seja removido, abra uma issue.
