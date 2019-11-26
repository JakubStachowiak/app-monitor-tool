**Żabka app monitor**

Aplikacja bazuje na **Jmeter** oraz **ElasticSearch** plus **Kibana**.

Podstawą do uruchomienia aplikacji jest obrac dokerowy : https://github.com/egaillardon/jmeter-plugins w wersji 5.2.0

Test wymaga aby obraz dokerowy zawierał zmienną środowiskową : **users_csv_path** wskazującą na plik z listą użytkowników, na bazie których będą wykonywane testy.
Aby było możliwe zapisanie danych w Elasticsearch'u, adres instancji musi być widoczny dla kontenera stworzonego na bazie obrazu z pluginami.
Aplikacja wymaga podania w zmiennych środowiskowych lokacji serwera ElasticSearch oraz Device ID
ELASTICSEARCH_HOST: host, pod którym zlokalizowany jest elasticsearch
ELASTICSEARCH_PORT: port, na jaki jmeter musi się odwołać aby połączyć się z elasticsearch'em
device_id: identyfikator urządzenia wykorzystywanego w testach
