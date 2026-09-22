# Projeto Dona Ju Confeitaria — V0.1

Fundação inicial de um PWA para controle de pedidos, produtos, clientes, estoque, entregas e relatórios.

## Estado atual

- Interface responsiva com identidade visual inspirada na logo enviada.
- Navegação entre Dashboard, Pedidos, Produtos, Clientes, Entregas e Relatórios.
- Dados de demonstração em memória do navegador.
- Formulários locais para cadastrar produtos, clientes e pedidos durante a demonstração.
- Manifest PWA inicial.
- Schema SQL inicial para Supabase.

## Próxima etapa

1. Criar o projeto no Supabase.
2. Executar e revisar `sql/schema.sql`.
3. Configurar autenticação dos dois usuários.
4. Criar policies RLS para limitar acesso aos usuários autorizados.
5. Substituir os dados locais pelo cliente Supabase.
6. Implementar movimentações transacionais de estoque e cálculo da validade na entrega.
7. Conectar os gráficos aos dados reais.

## Publicação no GitHub Pages

Envie os arquivos para um repositório e habilite GitHub Pages apontando para a branch/pasta escolhida.

**Segurança:** não coloque a `service_role key` do Supabase no código publicado. A chave anon/publishable deve ser usada com RLS configurado corretamente.
