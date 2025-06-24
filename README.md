# Repositório do *Dataset* de Acessibilidade em Artigos Acadêmicos (PDF)

Este repositório disponibiliza o conjunto de documentos classificados quanto à acessibilidade, organizado da seguinte forma:

```text
/class0   → PDFs não acessíveis
/class1   → PDFs acessíveis  
```

A rotulagem baseia‑se nos checkpoints do **Protocolo Matterhorn** analisados pelo **PDF Accessibility Checker (PAC)**.

---

## Índice
1. [Contexto da Acessibilidade em PDF](#contexto-da-acessibilidade-em-pdf)  
2. [Protocolo Matterhorn](#protocolo-matterhorn)  
3. [PDF Accessibility Checker (PAC)](#pdf-accessibility-checker-pac)  
4. [Referências](#referências)

---

## Contexto da Acessibilidade em PDF

Acessibilidade digital exige que conteúdos sejam utilizáveis por todas as pessoas, inclusive usuárias de tecnologias assistivas.  
Artigos científicos em **PDF** frequentemente carecem de marcação semântica, navegação por cabeçalhos e metadados de idioma, o que dificulta sua interpretação por leitores de tela.  
Embora a Lei nº 13.146/2015 (Lei Brasileira de Inclusão) assegure igualdade de acesso no ensino superior, estudos recentes revelam alta prevalência de falhas estruturais em repositórios institucionais e editoras comerciais.

---

## Protocolo Matterhorn

O **Matterhorn Protocol** (PDF Association, 2013 / rev. 2021) converte o padrão **PDF/UA (ISO 14289‑1)** em *136 condições de falha*:

| Bloco               | Exemplo de checkpoint | IDs Matterhorn |
|---------------------|-----------------------|----------------|
| Basic Requirements  | flag `/Tagged`        | 01–12, 18, 20–22, 30–31 |
| Logical Structure   | hierarquia de títulos | 09, 13–19, 27–28 |
| Metadata & Settings | idioma global         | 03–08, 23–26, 29 |

Neste *dataset*, falhas no grupo **PDF Syntax** implicam rótulo **não acessível**, independentemente das demais verificações.

---

## PDF Accessibility Checker (PAC)

[**PAC 2024**](https://www.axes4.com/) implementa a maioria dos checkpoints Matterhorn e produz três saídas principais:

* **Resumo** — aprovado, aviso *(warning)* ou reprovado  
* **Relatório técnico** — lista de falhas, localização e instruções de correção  
* **Árvore de tags** — visualização da estrutura lógica do documento  

Os resultados são agrupados em:

| Bloco PAC           | Itens verificados                                                                 |
|---------------------|-----------------------------------------------------------------------------------|
| Basic Requirements  | PDF Syntax, Fonts, Content, Embedded Files, Natural Language                      |
| Logical Structure   | Structure Elements, Structure Tree, Role Mapping, Alternative Descriptions        |
| Metadata & Settings | Metadata, Document Settings                                                       |

Falhas críticas em **PDF Syntax** (ex.: ausência da flag `/Tagged`) impedem a continuidade da auditoria e classificam o PDF como não acessível.

---

## Referências

- **Adobe.** *PDF Accessibility Overview*, 2023.  
- **axes4.** *PAC 2024 – PDF Accessibility Checker*, 2024.  
- **Brasil.** Lei nº 13.146 / 2015 (*Lei Brasileira de Inclusão*).  
- **Darvishy F. et al.** “Accessibility in Swiss Repositories”, 2023.  
- **Guimarães J.** “PDF Accessibility in Academic Publishing”, 2019.  
- **PDF Association.** *Matterhorn Protocol* v1.1, 2021.  
- **Pierres E.** “Semantic Tags in University Repositories”, 2024.  

*Todos os textos estão disponíveis em acesso aberto.*
