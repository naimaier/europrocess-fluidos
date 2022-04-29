# Sistema de Medição de Fluidos v2.0 - Europrocess
Página customizada para utilização no webserver do CLP Eliwell Free

## Adicionando imagens
As imagens são carregadas em série para evitar sobrecarregar o servidor com requests.
Para isso, as tags `<img>` devem ter o campo `src` em branco, e usaremos o seu `id` para carregarmos as imagens através da função `AddPreCacheImage()`.

## Gráfico
Utiliza a ferramenta https://dygraphs.com/ para gerar um gráfico em tempo real da leitura de temperatura do sistema.
Esses dados são armazenados na memória do cliente a partir do momento em que a página é carregada, mantendo os dados dos últimos 5 minutos.
O gráfico é mostrado quando um click é feito sobre o card do sensor de temperatura.