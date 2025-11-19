## Como revisar mudanças entre branches

Para garantir rastreabilidade e qualidade, sempre revise as diferenças entre a branch principal (`main`) e a branch de trabalho antes de integrar:

- **Via terminal:**
	```sh
	git diff main..nome-da-branch arquivo.extensao
	```
- **Via GitHub:**
	- Abra um Pull Request e utilize a aba "Files changed" para inspecionar todas as alterações.
- **Via ferramenta gráfica:**
	- Use o VS Code (Source Control > Compare with Branch) ou outra IDE para visualizar as diferenças de forma visual.

Recomenda-se revisar cada alteração, garantindo que apenas mudanças necessárias e aprovadas sejam integradas à branch principal.
# Sebo Online

![Livros](https://images.unsplash.com/photo-1512820790803-83ca734da794)

Bem-vindo ao projeto **Sebo Online**!

## Sobre o Projeto
O Sebo Online é uma plataforma para compra, venda e divulgação de livros, com seções especiais para:
- Produtos recém cadastrados
- Produtos raros
- Categorias

O objetivo é facilitar o acesso a livros novos e raros, promovendo a cultura e a leitura.

## Documentação do Workflow
Consulte o arquivo [WORKFLOW.md](./WORKFLOW.md) para conhecer o modelo de versionamento, convenção de commits e regras de colaboração adotadas pelo time.

## Estrutura do Projeto
| Seção                  | Descrição                                 |
|------------------------|-------------------------------------------|
| Produtos Recentes      | Livros recém adicionados ao catálogo      |
| Produtos Raros         | Edições especiais e exemplares únicos     |
| Categorias             | Organização dos livros por temas/assuntos |

## Como contribuir
1. Leia o [WORKFLOW.md](./WORKFLOW.md)
2. Crie uma branch a partir da `main`
3. Siga a convenção de commits semânticos
4. Abra um Pull Request para revisão

---

> Projeto desenvolvido para fins acadêmicos.
