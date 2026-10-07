# Dona Ju Confeitaria — V0.5.1

## O que mudou

### Interface
- Removidos os botões de ação do canto superior.
- Mantido um único FAB de ações no canto inferior.
- Dashboard também recebeu FAB para criar pedido.
- Navegação e cartões principais passaram a usar ícones SVG profissionais.
- Nenhum emoji é usado como ícone da interface.
- O cabeçalho ficou mais limpo e sem ações duplicadas.

### Banco
- Criada base Supabase multiusuário por confeitaria.
- RLS preparada para impedir acesso entre empresas.
- Histórico de pedidos, entregas, estoque e visitas estruturado.
- Snapshot de preço e custo nos itens do pedido para preservar histórico financeiro.
- View `v_customer_reorder_status` preparada para o ciclo de 10 dias.

## Próximo passo
V0.5.2 — autenticação e conexão real do frontend ao Supabase.
