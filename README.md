#### Wszystkie zmiany rób w klasie BooksController
#### Utworzyc zmienną przechowującą listę książek typu BooksList - w konstruktorze utworzyć jej instancję
#### Obsłużyć następujące requesty HTTP

- GET /books

    zwraca listę książek w jsonie np. [] i kod http 200 OK

- GET /books/book/{id}

    zwraca konkretną książkę dla podanego id i kod htt 200 OK

    gdy nie znajdzie książki to zwraca pustą body odpowiedzi i kod http 404 NOT_FOUND

- PUT /books/book/{id}

    zmienia name dla konkretnej książki na liście i zwraca zmienioną książkę i kod http 200 OK

    gdy nie znajdzie książki to zwraca pustą body odpowiedzi i kod http 404 NOT_FOUND

- POST /books

    dodaje nową książkę do listy przekazując w żądaniu parametr name z wartością

    zwraca true i kod http 200 OK

- DELETE /books/book/{id}

    usuwa konkretną książkę dla podanego id i kod htt 200 OK

    gdy nie znajdzie książki to zwraca pustą body odpowiedzi i kod http 404 NOT_FOUND

- DELETE /books
    usuwa wszystkie książki z listy i zwraca pustą listę i kod HTTP 200 ok

#### Pomoce

Aby uruchomić aplikację użyj Gradle albo Maven

Do tworzenia identyfikatorów wykorzystaj
```String uuid = UUID.randomUUID().toString();```

Do sprawdzania działania aplikacji możesz użyć kolekcji Postmana którą zaimportujesz do niego

[postman/Books.postman_collection.json](./postman/Books.postman_collection.json)

wszystkie potrzebne importy są w pliku klasy BooksController

przydatne aby zacząć - pokazuje jak zrobić obsługę requestu typu GET
https://spring.io/guides/gs/rest-service/