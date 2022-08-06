!!! tip "Site is currently under construction"
??? danger "Protect your identity"
    Exmuslims are in constant threat of [alienation, hostility and even death](https://persecution.exmuslims.org/). Make sure you are protecting your identity by [browsing anonymously](https://protonvpn.com/blog/how-to-be-anonymous-online/)!
# :material-database: Source Data
The ‘Source Data’ here means chapters and verses from Quran available for users to download in various formats.  Check out [Getting Started](../getting_started) to see how you can pull this data using Python.

## Chapters
[:material-web:](../../data/source/chapters.json) `https://projectq.io/data/source/chapters.json`

This dataset is a JSON list of dictionaries, where each dictionary has data on chapters, see example record below:
=== "Example record"
    ```json title="https://projectq.io/data/source/chapters.json"
    [
      {
        "id": 1,
        "name": "الفاتحة",
        "transliteration": "Al-Fatihah",
        "translation": "The Opener",
        "type": "meccan",
        "total_verses": 7
      },
      ...
    ]
    ```
=== "Reading in Python"

    Please see 'Reading Chapter List' in [Getting Started](../getting_started/#reading-chapter-list) 

## Individual Chapters
:material-web: `https://projectq.io/data/source/chapters/{n}.json`  
_Replace {n} with Chapter number_

This dataset is a JSON on individual chapter's data and includes verses as list of dictionaries, see example record below:

=== "Example record"
    ```json title="https://projectq.io/data/source/chapters/1.json"
    {
        "id": 1,
        "name": "الفاتحة",
        "transliteration": "Al-Fatihah",
        "translation": "The Opener",
        "type": "meccan",
        "total_verses": 7,
        "verses": [
            {
                "id": 1,
                "text": "بِسۡمِ ٱللَّهِ ٱلرَّحۡمَٰنِ ٱلرَّحِيمِ",
                "translation": "In the name of Allah, the Entirely Merciful, the Especially Merciful",
                "transliteration": "Bismi Allahi alrrahmani alrraheemi"
            },
            ...
        ]
    }
    ```
=== "Reading in Python"

    Please see 'Reading Single Chapter with verses' in [Getting Started](../getting_started/#individual-chapters) 

## Individual Verses with Multilingual Translations
:material-web: `https://projectq.io/data/source/verses/{n}.json`  
_Replace {n} with Verse number_

This dataset is a JSON on individual verss's data and includes multi-lingual translations, see example record below:

=== "Example record"
    ```json title="https://projectq.io/data/source/verses/1.json"
    {
        "id": 1,
        "number": 1,
        "text": "بِسۡمِ ٱللَّهِ ٱلرَّحۡمَٰنِ ٱلرَّحِيمِ",
        "translations": {
            "en": "In the name of Allah, the Entirely Merciful, the Especially Merciful",
            "es": "En el nombre de Dios, el Compasivo con toda la creación, el Misericordioso con los creyentes",
            "fr": "Au nom d'Allah, le Tout Miséricordieux, le Très Miséricordieux",
            "id": "Dengan nama Allah Yang Maha Pengasih, Maha Penyayang",
            "ru": "Во имя Аллаха, Милостивого, Милосердного",
            "sv": "I GUDS, DEN NÅDERIKES, DEN BARMHÄRTIGES NAMN",
            "tr": "Rahman ve Rahim olan Allah'ın adıyla",
            "ur": "اللہ کے نام سے جو رحمان و رحیم ہے",
            "zh": "奉至仁至慈的安拉之名"
        },
        "transliteration": "Bismi Allahi alrrahmani alrraheemi",
        "chapter": {
            "id": 1,
            "name": "الفاتحة",
            "transliteration": "Al-Fatihah",
            "translations": {
                "en": "The Opener",
                "es": "La Apertura",
                "fr": "L'ouverture",
                "id": "Pembukaan",
                "ru": "Открывающая Коран",
                "sv": "Öppningen",
                "tr": "Fâtiha",
                "ur": "کھولنے والی",
                "zh": "开端章"
            },
            "type": "meccan"
        }
    }
    ```
=== "Reading in Python"

    Please see 'Reading Individual Verses with Multilingual Translations' in [Getting Started](../getting_started/#reading-individual-verses-with-multilingual-translations) 

## All Verses with Extended Translations
[:material-web:](../../data/source/verses.json) `https://projectq.io/data/source/verses.json`  

This dataset is a JSON list of dictionaries, where each dictionary has data on verses including multiple translations in english, see example record below:

=== "Example record"
    ```json title="https://projectq.io/data/source/verses.json"
    [
      {
          "id": 1,
          "chapter": 1,
          "verse": 1,
          "Sahih_International": "In the name of Allah , the Entirely Merciful, the Especially Merciful.",
          "Yusuf_Ali": "In the name of Allah, Most Gracious, Most Merciful.",
          "Shakir": "In the name of Allah, the Beneficent, the Merciful.",
          "Muhammad_Sarwar": "In the Name of Allah, the Beneficent, the Merciful",
          "Mohsin_Khan": "In the Name of Allah, the Most Beneficent, the Most Merciful."
      },
      ...
    ]
    ```
=== "Reading in Python"

    Please see 'Reading All Verses with Extended Translations' in [Getting Started](../getting_started/#all-verses-with-extended-translations) 