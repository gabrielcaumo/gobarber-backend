# Recuperação de senha

**RF**
- O usuário deve poder recuperar sua senha informando o seu e-mail.
- O usuário deve receber um e-mail com instruções para recuperar a senha.
- O usuário deve poder redefinir sua senha.

**RNF**
- Utilizar Mailtrap para testar envios em ambiente de desenvolvimento.
- Utilizar Amazon SES para envios em produção.
- O envio de e-mail deve acontecer em segundo plano.

**RN**
- O link enviado por e-mail para redefinir a senha deve expirar em 2h.
- O usuário precisa confirmar a nova senha ao redefini-la.

# Atualização do perfil

**RF**
- O usuário deve poder atualizar seu nome, e-mail e senha.

**RN**
- O usuário não pode alterar seu e-mail para um e-mail já cadastrado.
- Para atualizar a senha, o usuário deve informar a senha antiga.
- Para atualizar a senha, o usuário deve confirmá-la.

# Painel do prestador

**RF**
- O usuário deve poder listar os seus agendamentos de um dia específico.
- O prestador deve receber uma notificação sempre que houver um novo agendamento.
- O prestador deve poder visualizar as notificações não lidas.

**RNF**
- Os agendamentos do prestador no dia devem ser armazenados em cache.
- As notificações do prestador devem ser armazenadas no MongoDB.
- As notificações do prestador devem ser enviadas em tempo real utilizando Socket.io.

**RN**
- As notificações devem ter um status de "lida/não lida" para que o prestador possa controlar.

# Agendamento de serviços

**RF**
- O usuário deve poder listar todos os prestadores de serviço cadastrados.
- O usuário deve poder listar os dias de um mês com pelo menos um horário disponível de um prestador.
- O usuário deve poder listar horários disponíveis em um dia específico de um prestardor.
- O usuário deve poder realizar um novo agendamento com um prestador.

**RNF**
- A listagem de prestadores deve ser armazenada em cache.

**RN**
- Cada agendamento de durar exatamente 1h.
- Os agendamentos devem ser disponibilizados das 8h às 17h.
- O usuário não pode agendar em um horário ocupado.
- O usuário não pode agendar em um horário que já passou.
- O usuário não pode agendar serviços consigo mesmo.
