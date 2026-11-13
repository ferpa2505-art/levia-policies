# Política de Privacidade — Leviã

**Última atualização:** 13 de novembro de 2026 · **Versão:** 2026-11-13

> **Resumo:** os registros de saúde que você anota no Leviã ficam no seu aparelho; o Leviã não recebe cópia deles. Para liberar o acesso, o atendimento pelo WhatsApp guarda seu nome, telefone, e-mail (se informado) e objetivo em nosso servidor. A análise de foto por IA é opcional, pede sua autorização antes do primeiro uso e envia só a foto do prato ao Google. Não vendemos dados e não exibimos anúncios. O pixel da Meta na página de vendas só funciona com o seu consentimento. O endereço IP é usado para segurança e limites de uso, com prazos definidos na seção 8.

## 1. Quem é o responsável

O Leviã é um aplicativo (Android e web/PWA) de registro pessoal de peso, alimentação, tratamento com medicamentos GLP-1 e diabetes.

- **Controlador (LGPD, art. 5º, VI):** Luis Fernando Paulino, pessoa física, que atua com o nome **FP Tech & Art**, Brasil.
- **Encarregado pelo tratamento de dados (LGPD, art. 41):** Luis Fernando Paulino.
- **Canal de privacidade e direitos:** **contato@leviapp.org**.

## 2. Dados em dois lugares

**No seu aparelho** ficam os registros que você escolhe fazer. **No servidor do Leviã** (Cloudflare) ficam apenas os dados necessários para liberar o acesso, controlar o uso e manter a segurança. As seções abaixo separam os dois.

## 3. Dados que ficam só no seu aparelho

- **Perfil:** nome, como prefere ser chamado(a), pronome, sexo biológico, idade, altura, peso, meta de peso e tipo de diabetes, se informados.
- **Peso e alimentação:** pesagens, refeições, alimentos, horários, calorias e nutrientes, água, receitas e exercícios.
- **Saúde:** doses e sintomas de GLP-1, glicemias e faixa-alvo, medicações, horários e observações.
- **Fotos de pratos:** no Android, uma cópia reduzida fica em arquivo no aparelho. No PWA, a foto reduzida é guardada como texto junto da refeição, no armazenamento do navegador.
- **Preferências:** idioma, tema, e-mail para relatórios (se informado), senha e biometria do app.

Parte disso são **dados pessoais sensíveis de saúde** (LGPD, art. 5º, II). Esses registros são criados e guardados por você, no seu aparelho; o Leviã não recebe cópia deles. Depois que você cria a senha do app, eles são **cifrados no aparelho** (AES-256-GCM) com uma chave de dados aleatória criada no seu aparelho. Como essa chave fica protegida depende de onde você usa o Leviã:

- **No celular (Android):** a chave de dados é protegida por uma chave guardada no cofre do sistema do aparelho (Android Keystore). Quem copiar só o armazenamento do app, por exemplo de um backup, não consegue abrir os registros sem essa chave do sistema. A senha do app funciona como trava do app, com limite de tentativas; ela não é a chave dos dados.
- **No navegador (PWA):** o navegador não tem cofre do sistema. A chave de dados é protegida por uma chave derivada da **sua senha** (Argon2id). **Atenção:** nesse caso a proteção contra quem copiar o armazenamento do navegador **depende de a senha ser longa e difícil de adivinhar**. Uma senha numérica curta, como um PIN de 4 a 10 dígitos, pode ser descoberta por quem tiver uma cópia dos dados do navegador, sem limite de tentativas. Prefira o celular para os registros mais sensíveis ou use uma senha longa.

Nada disso protege contra quem usa o aparelho **desbloqueado** com o app aberto, contra quem já sabe a senha, contra programas maliciosos com acesso total ao aparelho, nem contra uma cópia feita antes de você criar a senha: durante o cadastro, os registros ficam em texto no aparelho até essa etapa.

- **Senha esquecida, sem biometria ativada:** os dados ficam inacessíveis e não conseguimos recuperá-los. A única forma de restaurar é um backup feito antes.
- **Biometria ativada (celular):** o desbloqueio usa a biometria do próprio aparelho (digital ou rosto), gerida pelo sistema operacional. O Leviã recebe apenas "liberado" ou "não liberado"; **não recebe, não guarda e não analisa** sua digital, seu rosto ou qualquer dado biométrico. Você consegue trocar a senha sem perder os dados.
- Seu e-mail e a informação de que o cadastro foi concluído ficam guardados sem cifra, no armazenamento do app, para que o app saiba se deve pedir o cadastro.

## 4. Dados que ficam no servidor do Leviã

### 4.1 Atendimento pelo WhatsApp e acesso ao app

O acesso ao Leviã é liberado por um **serial** (código de ativação) enviado pelo WhatsApp. O atendimento é feito pelo **LEVI, um assistente virtual** (não é uma pessoa), em português (Brasil ou Portugal), inglês, espanhol ou italiano. Primeiro pedimos o seu **consentimento**, de forma destacada; só depois perguntamos seu **nome**, seu **e-mail** (opcional) e seu **objetivo**, que você escolhe em uma lista (por exemplo, emagrecer ou controlar diabetes, o que pode revelar uma condição de saúde). Se você responder "não", nada é guardado. Guardamos no servidor:

- nome, número de telefone, e-mail (se informado), objetivo escolhido, data e canal do consentimento;
- a etapa da conversa e identificadores técnicos das mensagens recebidas, para não repetir respostas;
- as mensagens que o LEVI ainda vai enviar a você (fila de envio, que inclui o texto da mensagem);
- uma conta com marcas irreversíveis (hash) do telefone e do e-mail; do serial guardamos apenas o hash, nunca o texto;
- os aparelhos ativados (um código aleatório por instalação, no máximo 2 por serial), as datas de uso e o período de teste ou assinatura.

**Lembretes:** se você parar de responder no meio do cadastro, o LEVI pode enviar até 3 lembretes (cerca de 30 segundos, 3 minutos e, no dia seguinte às 19h no fuso do país do seu número); quem consentiu também pode receber um vídeo de apresentação. Esses envios fazem parte da autorização pedida no início da conversa. Responda **PARAR** a qualquer momento e não escrevemos mais.

**Atendimento humano:** se o LEVI não conseguir ajudar, a conversa pode ser passada a uma pessoa da equipe, que poderá ler as mensagens trocadas.

### 4.2 Análise opcional da foto do prato por IA

A análise é **opcional**. Na primeira vez que você toca em **Analisar com IA**, o app mostra um aviso e só envia a foto se você concordar; se cancelar, nada é enviado. A autorização vale para as análises seguintes, e **cada foto só é enviada quando você toca no botão**. Para revogar, basta não usar mais o botão; para o aviso voltar a aparecer, limpe os dados do app neste aparelho. Como o Leviã não guarda as fotos, não há fotos nossas a apagar. O app envia ao servidor do Leviã: a foto reduzida (no máximo 1024 pixels), a licença do seu aparelho, o código aleatório da instalação, o idioma e dados técnicos da conexão (como o IP). O servidor confere a licença e os limites e encaminha **somente a foto** ao **Google Gemini**, que devolve a lista de alimentos e porções estimados.

- **Finalidade única:** identificar alimentos visíveis e estimar porções. O Leviã **não faz reconhecimento facial**, não cria modelos biométricos e não tenta identificar pessoas.
- Não enviamos nome, peso, glicemia, medicações ou outros registros.
- O Leviã não guarda a foto. O Google pode tratá-la por tempo limitado para prestar o serviço e detectar abuso, conforme os termos da API usada.
- A resposta volta ao aparelho e nada é salvo sem a sua confirmação. Você pode sempre registrar refeições à mão.
- Fotografe apenas o prato; **não inclua rostos, outras pessoas, documentos** ou outras informações pessoais.

Uma foto de prato pode, junto com o contexto do app, sugerir informação de saúde. Por isso tratamos o envio como **consentimento específico e destacado** (LGPD, art. 11, I).

### 4.3 Pagamentos

A assinatura é vendida pela **Hotmart**, que processa o pagamento: o Leviã não recebe nem guarda número de cartão. Da Hotmart recebemos o identificador da compra, o produto e o plano, o valor, a moeda, o status, as datas e os dados do comprador informados no checkout (nome, e-mail e telefone/WhatsApp), para liberar, renovar ou revogar o seu acesso e enviar o serial do plano. Guardamos um resumo desses eventos para comprovar a liberação, o cancelamento ou o reembolso. A Hotmart também trata os seus dados conforme a política dela.

### 4.4 Pixel de medição na página de vendas

Na página **www.leviapp.org**, se você aceitar no aviso de cookies, carregamos o pixel da **Meta** (Facebook e Instagram). Ele registra a visita à página, dados técnicos do navegador (incluindo endereço IP) e o clique no botão de assinatura com o plano e o valor escolhidos, para medir o desempenho de campanhas. **Nenhum dado de saúde é enviado**, e o pixel não é carregado se você recusar ou não responder. Você pode rever a escolha em "Preferências de cookies", no rodapé do site. Base legal: consentimento (LGPD, art. 7º, I).

### 4.5 Usos do endereço IP

O endereço IP é usado **só para segurança e controle de uso**, nunca para publicidade dentro do app:

- **Limites de uso da análise por IA e proteção contra abuso:** contadores por IP, por instalação e por conta, com janela de cerca de 1 hora; os registros são apagados automaticamente em até 31 dias.
- **Limite de tentativas de ativação do serial e de cadastro:** contadores por IP, apagados automaticamente em até 31 dias.
- **Registro de segurança das rotas administrativas:** o servidor tem rotas restritas à equipe (por exemplo, para publicar e medir a Página do Leviã no Facebook). Cada acesso a elas, autorizado ou não, gera um registro com a rota e o método, o **endereço IP** de quem chamou, o resultado (código e motivo), um detalhe técnico curto e a data e a hora. **Não guardamos** senhas ou tokens, cabeçalhos de autenticação, o corpo da requisição nem o texto publicado. Prazo: 180 dias, com apagamento automático diário.
- **Registros operacionais da Cloudflare**, que hospeda o servidor, seguem a retenção do serviço contratado.

Base legal: legítimo interesse e segurança (LGPD, art. 7º, IX), usando só o mínimo necessário, e, quando aplicável, cumprimento de obrigação legal (art. 7º, II).

### 4.6 E-mail

Quando você informa seu e-mail, ele pode ser usado para enviar o acesso de teste e avisos importantes sobre a sua conta. O envio é feito pela **Resend**. A equipe também recebe por e-mail alertas internos (por exemplo, pedido de atendimento humano ou falha de pagamento), que podem conter o necessário para resolver o seu caso.

## 5. Base legal

- **Consentimento específico e destacado** (LGPD, arts. 7º, I e 11, I): guardar nome, telefone, e-mail e objetivo no atendimento pelo WhatsApp (o objetivo pode revelar dado de saúde) e enviar os lembretes do cadastro; enviar cada foto à IA (seção 4.2); pixel de medição da página de vendas (seção 4.4). Você pode revogar a qualquer momento (seção 9), sem prejuízo do que já foi feito.
- **Execução de contrato** (art. 7º, V): liberar e manter seu acesso, emitir o serial e processar a assinatura.
- **Legítimo interesse e segurança** (art. 7º, IX): limitar abuso, prevenir fraude e registrar acessos às rotas administrativas (seção 4.5).
- **Obrigação legal e exercício regular de direitos** (art. 7º, II e VI; art. 16): guardar registros de pagamento, reembolso e segurança pelo prazo que a lei exigir ou enquanto necessários para defesa em processos.

## 6. Com quem compartilhamos e transferência internacional

Usamos estes prestadores para operar o serviço, cada um só com o necessário:

| Prestador | Para quê | Dados |
|---|---|---|
| **Cloudflare** | hospedagem do servidor, banco de dados e site | dados do servidor (seção 4), IP |
| **Hetzner** (Finlândia) | servidor que mantém a conexão com o WhatsApp | telefone, mensagens em trânsito, credenciais da conexão |
| **Meta / WhatsApp** | canal de conversa; pixel da página de vendas (só com consentimento); publicação na Página do Leviã | mensagens; dados do pixel (seção 4.4) |
| **Google (Gemini)** | análise da foto, só quando você pede | foto reduzida |
| **Hotmart** | pagamentos | dados da compra (seção 4.3) |
| **Resend** | envio de e-mail | e-mail e conteúdo da mensagem |
| **Expo** | atualizações do aplicativo | dados técnicos do aparelho; nenhum registro seu |

Também baixamos notícias públicas de sites de saúde; nenhum registro seu vai nessas requisições. Não vendemos nem alugamos dados.

**Transferência internacional:** alguns desses prestadores tratam dados fora do Brasil (por exemplo, nos Estados Unidos e na União Europeia). Essas transferências são feitas apenas para prestar o serviço, com o mínimo de dados, conforme o art. 33 da LGPD e a Resolução CD/ANPD nº 19/2024, com base nas garantias contratuais de proteção de dados oferecidas por cada prestador. Pelo canal da seção 1 você pode pedir o país e a garantia aplicável a cada prestador.

## 7. Backup, relatórios e exportação

O arquivo de backup ou relatório é criado no seu aparelho e só sai dele para o destino que você escolher. O backup pode ser protegido com senha (AES-256-GCM); nós não temos a senha nem como recuperá-la. O identificador de instalação e a licença não entram no backup. **Atenção:** no Android as fotos dos pratos não entram no backup; no PWA elas ficam dentro do registro da refeição e **entram no arquivo**. Guarde o arquivo com cuidado, de preferência com senha.

## 8. Por quanto tempo guardamos

| Dado | Prazo |
|---|---|
| Registros no aparelho | até você apagar, desinstalar o app ou limpar os dados |
| Nome, telefone, e-mail, objetivo, consentimento, conta, serial (hash) e aparelhos | enquanto a conta existir ou até você pedir a exclusão |
| Conversa de cadastro não concluída | cerca de 3 dias |
| Identificadores técnicos das mensagens recebidas | 30 dias |
| Fila de mensagens a enviar (inclui o texto) | até 14 dias, ou antes, se você pedir a exclusão |
| Contadores de uso e de tentativas (incluem IP ou código da instalação) | até 31 dias |
| Registro de segurança das rotas administrativas | 180 dias |
| Resumo de eventos de pagamento e reembolso | pelo prazo legal e enquanto necessário para defesa de direitos |
| Foto enviada à IA | não guardada pelo Leviã; retenção pelo Google conforme os termos dele |

## 9. Seus direitos e exclusão

Pelo art. 18 da LGPD você pode pedir: confirmação de que tratamos seus dados, acesso, correção, anonimização, bloqueio ou eliminação de dados desnecessários, portabilidade, eliminação dos dados tratados com consentimento, informação sobre com quem compartilhamos, informação sobre a possibilidade de não consentir e **revogação do consentimento**.

- **Como pedir:** escreva para **contato@leviapp.org** informando o telefone usado no WhatsApp. Podemos pedir uma confirmação de identidade para proteger sua conta.
- **Prazos:** a confirmação e o acesso em formato simplificado são respondidos de imediato quando possível; a declaração completa, em até **15 dias** do pedido (LGPD, art. 19). Os demais pedidos são atendidos sem demora; se não pudermos atender de imediato, explicamos o motivo e o prazo.
- **Exclusão pelo WhatsApp:** responda **APAGAR**. Apagamos seu cadastro, sua conta, o serial, os aparelhos ativados, o teste ou assinatura vinculados e as mensagens na fila de envio; o serial e os aparelhos deixam de valer. **Não são apagados na hora:** os contadores técnicos de uso (apagam sozinhos em até 31 dias), os identificadores técnicos de mensagens (30 dias), o resumo de eventos de pagamento (guardado pelo prazo legal), o registro de segurança (180 dias) e as cópias mantidas pelos próprios prestadores, como o histórico da conversa no WhatsApp e os dados da compra na Hotmart, que seguem as políticas deles.
- **Parar mensagens:** responda **PARAR**.
- Você também pode reclamar à Autoridade Nacional de Proteção de Dados (ANPD).

## 10. Segurança e incidentes

Usamos conexão cifrada (HTTPS), guardamos o serial e as marcas de telefone e e-mail apenas como hash, assinamos as licenças, limitamos tentativas, registramos o acesso às rotas administrativas e mantemos as chaves fora do código. Nenhum sistema é 100% seguro.

Se ocorrer um incidente de segurança que possa causar risco ou dano relevante a você, comunicaremos a **ANPD** e **você** em até **3 dias úteis** contados do momento em que soubermos que o incidente afetou dados pessoais, conforme a Resolução CD/ANPD nº 15/2024 (observado o prazo diferenciado previsto para agentes de pequeno porte, quando aplicável). A comunicação dirá o que aconteceu, quais dados foram afetados, os riscos e o que fazer. Mantemos registro de todo incidente por pelo menos 5 anos.

## 11. Crianças e aviso de saúde

O Leviã não é destinado a menores de 18 anos. É uma ferramenta de registro e organização pessoal: não faz diagnóstico, não prescreve tratamento e não substitui médico, nutricionista ou outro profissional de saúde.

## 12. Mudanças nesta política

Se passarmos a tratar outros dados ou usar outros serviços, atualizaremos esta política antes de o recurso entrar no ar, com a data e a versão no topo. Mudanças relevantes serão avisadas no app ou pelo WhatsApp e, quando dependerem de consentimento, pediremos de novo.

---

Leia também os [Termos de Serviço](https://leviapp.org/termos).
