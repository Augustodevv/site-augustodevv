# Site Augusto Novaes

Site de prestação de serviço — **landing pages e sites institucionais** para
pequenos negócios e profissionais autônomos.

Feito em HTML, CSS e JavaScript puro. Sem build, sem dependências, sem banco
de dados.

---

## Como abrir

**Opção 1 — abrir o arquivo**

Dê dois cliques em `index.html`. Funciona direto no navegador.

**Opção 2 — servir por HTTP (recomendado para testar no celular)**

```bash
python -m http.server 8000
```

Acesse `http://localhost:8000`. Para abrir no celular, use o IP da sua máquina
na mesma rede, por exemplo `http://192.168.0.10:8000`.

---

## Como publicar

O site é estático: basta subir os arquivos para qualquer hospedagem estática.

| Serviço | Como |
| --- | --- |
| **Netlify Drop** | arraste a pasta em [app.netlify.com/drop](https://app.netlify.com/drop) |
| **GitHub Pages** | Settings → Pages → Source: branch `main`, pasta `/ (root)` |
| **Vercel** | `npx vercel --prod` |
| **Cloudflare Pages** | Conecte o repositório, sem comando de build |

Para **GitHub Pages**, o site fica disponível em
`https://augustodevv.github.io/site-augustodevv/`.

---

## Estrutura

```
index.html                              página completa (8 seções)
style.css                               estilos e animações
script.js                               interações (menu, FAQ, efeitos)
assets/images/brand/logo-augusto.svg    logo
```

### Seções da página

1. **Início** — apresentação e chamada para o WhatsApp
2. **Serviços** — landing page e site institucional
3. **Projeto** — demonstração de um site entregue
4. **Processo** — as 5 etapas, do primeiro contato à publicação
5. **Sobre** — quem é o Augusto
6. **Em evolução** — automações, agentes de IA e sistemas web
7. **Dúvidas frequentes**
8. **Contato** — WhatsApp, telefone e e-mail

---

## Contato

- **WhatsApp:** (12) 99600-1610 · [wa.me/5512996001610](https://wa.me/5512996001610)
- **E-mail:** augustonovaes25@gmail.com
- **LinkedIn:** [linkedin.com/in/augustonovaesdev](https://www.linkedin.com/in/augustonovaesdev)
- **Portfólio:** [augustodev.com](https://www.augustodev.com)

---

## O que revisar antes de publicar

**1. Seção "Projeto"**

Hoje é um projeto de **demonstração** ("Landing Aurora"), usado para mostrar o
padrão de entrega já que não havia case publicado. Para trocar pelo projeto real,
edite em `index.html`:

- o título em `<h2 id="projects-title">`
- o texto em `.case-intro > .case-context`
- as tags em `.case-tags`
- o link do botão "Meu portfólio" (`.case-status`)
- as duas prévias de tela

**2. Prévias do projeto**

As telas de desktop e celular são **desenhadas com CSS** (sem arquivos de
imagem), então o site não depende de pictures. Se você tiver capturas de tela
reais, substitua o conteúdo de `.project-preview` por `<img>`.

**3. Preços e prazos**

O FAQ não cita valores. Para publicar preços, edite os itens "Quanto custa um
site?" e "Quanto tempo leva?" em `index.html`.

**4. Links do rodapé**

Hoje: LinkedIn, e-mail e WhatsApp. Se quiser, troque o LinkedIn por Instagram.

---

## Acessibilidade e desempenho

- HTML semântico com `skip link` e `aria-label` nos controles
- Respeita `prefers-reduced-motion` — desliga as animações para quem pediu
- Menu móvel com teclado, `Escape` e foco devolvido
- FAQ em `<details>` nativo, funciona sem JavaScript
- Conteúdo visível mesmo com JavaScript desativado

---

© Augusto Novaes