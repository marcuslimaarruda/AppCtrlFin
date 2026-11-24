# Histórico de versões

## Próxima versão

- **Dados numa pasta nova:** `%USERPROFILE%\Time2Fin` (a pasta *Time2Fin* dentro da sua pasta de usuário). Na primeira abertura o app copia seus dados e as cópias de segurança da pasta antiga (`%LOCALAPPDATA%\AppCtrlFin`), que fica intacta como reserva. É o que permite publicar o app na Microsoft Store sem risco de perder dados ao desinstalar.
- **Simulador de cenários de investimento** (Investimentos → *Simular cenários*, no computador e no celular): divida o dinheiro entre opções (CDB, LCI/LCA, Tesouro IPCA+, prefixado, ações…), diga como cada uma rende e veja o resultado líquido de IR nos cenários pessimista, base e otimista, em dinheiro de hoje (sem a inflação) e comparado a deixar tudo num CDB de 100% do CDI. Começa com os seus investimentos de hoje; o botão *Exemplo* traz uma divisão para editar. É só cálculo com as suas premissas, não recomendação. A última simulação fica guardada e vai para o outro aparelho na sincronização.

## 0.2.0-teste.2 — versão de teste (18/11/2026)

- **Novo nome: Time2Fin** (antes AppCtrlFin), com logo novo (peixe-boi e filhote). Seus dados continuam na mesma pasta e nada muda no uso; a sincronização com o celular continua funcionando com aparelhos já pareados.
- **Meta "guardar por mês"** (ex.: R$ 1.000/mês para a entrada do carro), no computador e no celular:
  - a tela diz na hora se a meta é viável, isto é, se a conta fecha todos os meses sem resgatar investimentos;
  - quando não é, sugere mais tempo com o mesmo total, valor menor no mesmo prazo ou começar depois;
  - viável, ao salvar vira um compromisso mensal: uma parcela por mês no tipo "🎯 Metas" da tela principal, que reúne todas as metas ("Entrada do carro — 3/12"); a meta mostra quanto já foi juntado;
  - mudou o valor ou os meses: as parcelas não pagas são refeitas;
  - guardou um valor diferente num mês: o app oferece diluir a diferença nas próximas parcelas, mudar o prazo ou deixar como está, dizendo se cada opção cabe no orçamento.
- **Descartar simulação:** num mês futuro, uma linha simulada pode ser descartada só naquele mês ou dali em diante (ex.: salário depois de sair do emprego). Para restaurar, use o aviso no rodapé.
- **Tipos de transação:** a coluna Ativo pode ser marcada ou desmarcada direto na grade.
- **Descrição do lançamento:** campo novo, que aparece nos itens da tela principal (o grupo continua com o nome do tipo). Na atualização, o texto das observações passa para a descrição.
- **Tipos de transação sem código:** basta o nome; o código interno é gerado sozinho.
- **Cor do tipo de transação:** escolhida no cadastro (paleta, outra cor ou sem cor). A linha aparece nessa cor na tela principal e, no celular, como uma faixa ao lado do nome.
- **Compras do cartão mais rápidas:**
  - digitação direto na grade: data curta ("8"), descrição com sugestões e valor; Enter grava e passa para a próxima;
  - importação do extrato do banco em OFX ou CSV, com conferência linha a linha;
  - o mesmo arquivo pode ser importado várias vezes, porque só entram compras novas e compras já digitadas não duplicam;
  - banco emissor no cadastro do cartão.
- **Resumo do mês no celular:**
  - o cartão da conta mostra início + entradas − saídas = projeção;
  - cada lançamento ocupa uma linha ("Feira · Pago em 03/11");
  - a cor do tipo aparece também no fundo dos lançamentos;
  - tocar no tipo recolhe ou expande os lançamentos dele.
- **App do celular, etapa 3:** digitação rápida de compras, importação de extrato (OFX/CSV) com conferência e banco emissor no cadastro do cartão. O celular passa a ter as mesmas funções do computador.
- **App do celular, etapa 2:** visão global (estimado em resumo anual, realizado, metas e premissas), cadastro de metas e premissas e os parâmetros (nascimento, idade final, mês marcador).
- **App do celular, etapa 1:** conta corrente (extrato do mês e socorro pelo investimento) e investimentos (lista, saldo, mês a mês, aplicar, resgatar, atualizar saldo e cadastro).
- **Sincronização com o celular pelo Wi-Fi:**
  - o botão *Celular...* mostra um QR Code; o celular lê o código (ou o usuário digita) e os dados ficam iguais nos dois aparelhos, sem internet e sem conta;
  - na primeira vez, o celular recebe tudo do computador; depois, só o que mudou vai e volta, e vale a alteração mais recente;
  - dados cifrados com o código do computador;
  - compras do mesmo cartão lançadas nos dois aparelhos somam no total da fatura;
  - banco versão 6.
- **Abas com mais contraste** (Visão global e Investimentos): a aba aberta fica destacada em verde com texto branco, e as outras em cinza.
- **Proteção dos dados:**
  - cópia automática do banco antes de atualizar a estrutura;
  - ao instalar por cima de dados existentes, pergunta se mantém os dados ou recomeça (recomeçar guarda uma cópia);
  - com o banco vazio e cópias com dados na pasta, oferece restaurar;
  - limpeza automática: ficam as 10 cópias mais recentes e as do último mês.

## 0.1.0 — primeira versão de distribuição

- **Tela principal:** controle mensal com saldo de hoje, projeção do fim do mês e simulação de meses futuros.
- **Lançamentos:** previsto e realizado, com confirmação de pagamento. O app avisa quando o pagamento fica fora do mês do vencimento.
- **Tipos de transação:** crédito ou débito; tipos compostos por eventos (cartões, com dia de corte e vencimento).
- **Cartões:** compras, estornos e parcelas; a fatura do mês se monta sozinha; confirmação do pagamento da fatura na tela de compras.
- **Conta corrente:** extrato mensal com aviso de saldo negativo e socorro pelo investimento marcado.
- **Investimentos:** aplicações, resgates, rendimentos, movimentação mensal, projeção e investimentos encerrados.
- **Visão global:** realizado, estimado pelas premissas, metas com ajuste mensal necessário e mês marcador do ano.
- **Banco:** SQLite local, criado zerado na instalação, com os tipos de transação padrão.
- **Documentação:** manual do usuário no app (botão **? Manual**) e vídeo de apresentação narrado, com legendas.
