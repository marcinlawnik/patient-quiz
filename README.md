# patient-quiz

## Założenia

Celem aplikacji jest ziwększenie świadomości pacjentów co do ich choroby/zaleceń pozabiegowych, co wpłynie na poprawę stanu zdrowia.

## Ekrany aplikacji

### Ekran główny

Na głównym ekranie znajduje się lista tematów, które są zawarte w aplikacji. Lista jest pobierana z serwera. Każdy temat zawiera materiały (w formie HTML) oraz pytania z odpowiedziami. Po wyborze tematu przechodzimy do danego ekranu informacyjnego.

Lista tematów jest w formie pliku topics.json:

```
{
  "topics": [
    {
      "id": 1234,
      "description": "Operacja na oczy"
    },
    {
      "id": 552,
      "description": "Operacja na uszy"
    },
    {
      "id": 12,
      "description": "Operacja na nos"
    },
    {
      "id": 14,
      "description": "Operacja na pięty"
    }
  ]
}
```

### Ekran informacyjny

Tutaj wyświetlane są materiały pobrane z serwera w formie JSON. Mogą być podzielone na strony, fajnie jakby dodatkowo była opcja zwiększenia czcionki. Content jest w formacie HTML więc należy obsługiwać np. obrazki lub wideo. Od razu przesyłane są też pytania i odpowiedzi. Po przeczytaniu klika się "Przejdź do quizu".


```
{
  "topic": {
    "id": 1234,
    "title": "Operacja na oczy",
    "content": "Operację na oczy można wykonać <b>Bardzo ostrożnie</b>.",
    "questions": [
      {
        "question": "Czy można otworzyć oczy?",
        "answers": [
          {
            "answer": "tak",
            "isCorrect": true
          },
          {
            "answer": "nie",
            "isCorrect": false
          },
                    {
            "answer": "może",
            "isCorrect": false
          },
          {
            "answer": "nie wiem",
            "isCorrect": false
          }
        ]
      },
      {
        "question": "Czy można otworzyć nos?",
        "answers": [
          {
            "answer": "tak",
            "isCorrect": true
          },
          {
            "answer": "nie",
            "isCorrect": false
          },
                    {
            "answer": "może",
            "isCorrect": false
          },
          {
            "answer": "nie wiem",
            "isCorrect": false
          }
        ]
      },
            {
        "question": "Czy można otworzyć uszy?",
        "answers": [
          {
            "answer": "tak",
            "isCorrect": false
          },
          {
            "answer": "nie",
            "isCorrect": false
          },
                    {
            "answer": "może",
            "isCorrect": false
          },
          {
            "answer": "nie wiem",
            "isCorrect": true
          }
        ]
      }
    ]
  }
}
```

### Quiz

Quiz ma pytania i odpowiedzi jednokrotnego wyboru (w przyszłości także wielokrotnego wyboru, isCorrect w wielu odpowiedziach = true). Po podsumowaniu i sprawdzeniu odpowiedzi wynik jest zapisywany.

### Ekran finalny

Na tym ekranie użytkownik wpisuje swoje imię, i po wpisaniu wynik quizu i imię są wysyłane na serwer.

## Ustalenia

Na razie pliki JSON możesz otwierać z aplikacji, w tygodniu przygotuję je tak żeby były w internecie.
W razie pytań marcin@lawniczak.me 




