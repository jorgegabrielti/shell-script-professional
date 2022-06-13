# Capítulo 2 - Controle de qualidade

Created: June 13, 2022 3:36 PM

# Prefácio

Um bom profissional sabe como fazer um trabalho de qualidade. Isso faz parte do seu dia a dias, não é preciso se esforçar. A atenção aos detalhes e a buscas por um resultado perfeito são algumas de suas características. Aprenda quais são os componentes que farão seu programa em shell ser considerado profissional. Destaque-se, faça o melhor, faça o todo.

## Codificação limpa

Existem várias maneiras de se deixar o código de um programa mais amigável e informativo. Algumas delas, entre outras que veremos adiante:

- Cabeçalho inicial com um explicação geral do funcionamento.
- Código alinhado (indent) e bem-espaçado verticalmente.
- Comentários explicativos e esclarecedores.
- Nomes descritivos para funções e variáveis.
- Controle de alterações e versões.
- Estrutura interna coesa e padronizada.

### Extras

Além disso, um programa ainda pode ter extras para torná-lo mais profissional:

- Manual de uso.
- Manual técnica.
- Suíte de testes.
- Registro histórico das mudanças (Changelog).
- Base de problemas conhecidos.
- Versões beta.
- Arquivos de exemplo de comportamento (se aplicável).

## Cabeçalho inicial

O cabeçalho inicial é a primeira parte do programa, o primeiro texto que qualquer um que for ler seu código-fonte irá encontrar. Pelo seu posicionamento, é aconselhável colocar neste cabeçalho todas as informações necessárias para que o leitor tenha uma visão geral do programa. Como sugestão, este é o formato de um cabeçalho informativo:

- Localização (`path`) do interpretador.
- Nome do programa.
- Descrição breve do propósito.
- Site do programa (se aplicável).
- Nome do autor.
- E-mail do autor.
- Nome e e-mail do responsável pela manutenção (caso diferente do autor).
- Descrição detalhada do funcioamento.
- Data de criação.
- Histórico de mudanças (data, nome, descrição).
- Licença (copyright).

Exemplo de cabeçalho:

```bash
#!/bin/bash
#
# nome_completo.sh - Busca o nome completo de um usuário no Unix
#
# Site      : http://programas.com.br/nomecompleto/
# Autor     : João Silva <joao@email.com.br>
# Manutenção: Maria Teixeira <maria@email.com.br>
#
#  -------------------------------------------------------------
#   Este programa recebe como parâmetro o login de um usuário e
#   procura em várias bases qual o seu nome completo, retornando
#   o resultado na saída padrão (STDOUT).
#
#   Exemplos:
#      $ ./nome_completo.sh jose
#      José Moreira
#      $ ./nome_completo.sh joseee
#      $
#
#   A ordem de procura do nome completo é seqüencial:
#
#      1. Arquivo /etc/passwd
#      2. Arquivo $HOME/.plan
#      3. Base de Usuários LDAP
#      4. Base de Usuários MySQL
#
#   Respeitando a ordem, o primeiro resultado encontrado será o
#   retornado.
#  -------------------------------------------------------------
#
#
# Histórico:
#
#    v1.0 1999-05-18, João Silva:
#       - Versão inicial procurando no /etc/passwd
#    v1.1 1999-08-02, João Silva:
#       - Adicionada pesquisa no $HOME/.plan
#       - Corrigido bug com nomes acentuados
#    v2.0 2000-04-28, Mário Rocha:
#       - Corrigidos 2.534 bugs (O João não sabe programar!)
#       - Adicionado meu nome em vários lugares hehehe
#    v2.1 2000-04-30, José Moreira:
#       - Desfeitas as "correções" do Mário (ele quebrou o programa)
#       - Retirada a frase "Mário é o Maior" de várias partes
#    v2.2 2000-05-02, José Moreira:
#       - Adicionado suporte a LDAP (que trabalheira!)
#       - Aceita nomes de usuários EM MAIÚSCULAS
#       - Retirado suporte a acentuação (estraga meu terminal)
#    v2.3 2000-05-03, José Moreira:
#       - Arrumado o suporte a LDAP (agora vai funcionar)
#    v2.4 2000-05-03, José Moreira:
#       - Arrumado o suporte a LDAP (agora é pra valer)
#    v2.5 2000-05-04, José Moreira:
#       - Retirado o suporte a LDAP (eu odeio LDAP!)
#    v3.0 2000-05-10, Maria Teixeira:
#       - Programa reescrito do zero
#       - Adicionado suporte a LDAP (funcional)
#       - Adicionado suporte a MySQL
#       - Restaurado suporte a acentuação
#    v3.1 2003-05-10, Maria Teixeira:
#       - Adicionado este comentário para comemorar 3 anos sem
#         alterações :)
#
#
# Licença: GPL.
#
```