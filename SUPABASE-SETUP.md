# Dona Ju Confeitaria — V0.5.1

Esta versão prepara a base do sistema para sair do armazenamento local e usar Supabase.

## 1. Criar o projeto

No Supabase, crie um projeto novo para a Dona Ju Confeitaria.

## 2. Criar as tabelas

Abra **SQL Editor** e execute o arquivo:

`sql/schema.sql`

Ele cria:
- empresa/confeitaria;
- perfis e permissões básicas;
- clientes;
- produtos;
- pedidos e itens;
- movimentos de estoque;
- entregas;
- histórico de visitas;
- notificações;
- índices;
- RLS;
- visão do ciclo de recompra de 10 dias.

## 3. Criar os dois administradores

Crie os dois usuários em **Authentication > Users**.

Depois, crie a empresa em `businesses` e associe os dois usuários em `profiles`, usando o mesmo `business_id`.

Exemplo conceitual:

```sql
insert into public.businesses (name, slug)
values ('Dona Ju Confeitaria', 'dona-ju')
returning id;
```

Com o UUID retornado, associe os usuários:

```sql
insert into public.profiles (id, business_id, full_name, role)
values
  ('UUID_DO_USUARIO_1', 'UUID_DA_EMPRESA', 'Administrador 1', 'admin'),
  ('UUID_DO_USUARIO_2', 'UUID_DA_EMPRESA', 'Administrador 2', 'admin');
```

## 4. Segurança

A aplicação usa a chave pública/anon do Supabase no navegador. **Nunca coloque a `service_role` no GitHub Pages.**

## 5. Próxima etapa

V0.5.2 será a camada de autenticação/login e conexão do frontend com o Supabase, preservando esta interface.
