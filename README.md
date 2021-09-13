# Quran Dataset MongoDB

Dataset MongoDB Al-Qur'an in Bahasa Indonesia

>Thanks to Mas Rio Astamal (@rioastamal) who provide Al-Quran dataset at https://github.com/rioastamal/quran-json



## How to Use
1. Download/Clone repo
2. Open terminal and run this command
```bash
mongorestore --db dbname 
```
3. Done

## Format Collection

### ayat

Format

```json
"_id": "ObjectID",
"number": "str",
"name": "str",
"name_latin": "str",
"number_of_ayah": "str",
"text": {
    "num_of_ayat": "str"
},
"translation": {
    "(lang)": {
        "name": "str",
        "text": {
            "num_of_ayat": "str"
        }
    }
},
"tafsir": {
    "(lang)": {
        "(source)": {
            "name": "str",
            "source": "str",
            "text": {
                "num_of_ayat": "str"
            }
        }
    }
}
```

Example
QS. Al Fatihah

```json
{
    "_id" : ObjectId("xxx"),
    "number" : "1",
    "name" : "الفاتحة",
    "name_latin" : "Al-Fatihah",
    "number_of_ayah" : "7",
    "text" : {
        "1" : "بِسْمِ اللّٰهِ الرَّحْمٰنِ الرَّحِيْمِ",
        "2" : "اَلْحَمْدُ لِلّٰهِ رَبِّ الْعٰلَمِيْنَۙ",
        "3" : "الرَّحْمٰنِ الرَّحِيْمِۙ",
        "4" : "مٰلِكِ يَوْمِ الدِّيْنِۗ",
        "5" : "اِيَّاكَ نَعْبُدُ وَاِيَّاكَ نَسْتَعِيْنُۗ",
        "6" : "اِهْدِنَا الصِّرَاطَ الْمُسْتَقِيْمَ ۙ",
        "7" : "صِرَاطَ الَّذِيْنَ اَنْعَمْتَ عَلَيْهِمْ ەۙ غَيْرِ الْمَغْضُوْبِ عَلَيْهِمْ وَلَا الضَّاۤلِّيْنَ ࣖ"
    },
    "translations" : {
        "id" : {
            "name" : "Pembukaan",
            "text" : {
                "1" : "Dengan nama Allah Yang Maha Pengasih, Maha Penyayang.",
                "2" : "Segala puji bagi Allah, Tuhan seluruh alam,",
                "3" : "Yang Maha Pengasih, Maha Penyayang,",
                "4" : "Pemilik hari pembalasan.",
                "5" : "Hanya kepada Engkaulah kami menyembah dan hanya kepada Engkaulah kami mohon pertolongan.",
                "6" : "Tunjukilah kami jalan yang lurus,",
                "7" : "(yaitu) jalan orang-orang yang telah Engkau beri nikmat kepadanya; bukan (jalan) mereka yang dimurkai, dan bukan (pula jalan) mereka yang sesat."
            }
        }
    },
    "tafsir" : {
        "id" : {
            "kemenag" : {
                "name" : "Kemenag",
                "source" : "Aplikasi Quran Kementrian Agama Republik Indonesia",
                "text" : {
                    "1": "xxx",
                    "2": "xxx",
                    "3": "xxx",
                    "4": "xxx",
                    "5": "xxx",
                    "6": "xxx",
                    "7": "xxx"
                }
            }
        }
    }
}

```