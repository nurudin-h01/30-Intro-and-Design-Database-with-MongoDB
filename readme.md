# 1. Relasi Skiljek dan Schema.

Jenis Relasi One-to-one

```json
{
	"_id": "ObjectId('61bb47fd265744521cdd176f')",
	"fullName": "John Doe",
	"email": "john123@mail.com",
	"phoneNumber": "0812345678910"
}
```

<br>

# 2. Relasi SkilShop dan Schema.

Jenis Relasi One-to-few

```json
{
	"_id": "ObjectId('61bbaf56dc8178701f2fd55b')",
	"fullName": "John Doe",
	"phoneNumber": "0812345678910",
	"address": [
		{ "street": "Jalan Malang", "city": "Malang" },
		{ "street": "Jalan Batu", "city": "Batu" }
	]
}
```

<br>

# 3. Relasi SkilShop dan Schema

Relasi: One-to-many

```json
{
	"_id": "ObjectId('61bbafc2bebd7b2275d26179')",
	"productName": "Kaos Polos",
	"brandName": "SkilShirt",
	"variants": [
		{
			"variantName": "Kaos Polos Hitam",
			"color": "Hitam",
			"quantity": 12,
			"price": "Rp 99.000"
		},
		{
			"variantName": "Kaos Polos Navy",
			"color": "Navy",
			"quantity": 10,
			"price": "Rp 99.000"
		}
	]
}
```

<br>

# 4. Relasi SkilFlix dan Schema

Jenis Relasi Many-to-many

Cinema:

```json
{
  "_id": "ObjectId('61bbafc3bebd7b2275d2617b')",
  "films": [
    "ObjectId('61bbafc4bebd7b2275d2617d')",
    "ObjectId('61bbafc5bebd7b2275d2617f')"
  ],
  "cinemaName": "CGF",
  "location": "Pondok Indah Mall"

},
{
  "_id": "ObjectId('61bbb6751b06f1948c798d70')",
  "cinemaName": "Cinema31",
  "films": [
    "ObjectId('61bbafc4bebd7b2275d2617d')",
    "ObjectId('61bbafc5bebd7b2275d2617f')"
  ],
  "location": "Mall Kelapa Gading"

}
```

Movie:

```json
{
  "_id": "ObjectId('61bbafc4bebd7b2275d2617d')",
  "filmName": "Venom 2",
  "cinemas": [
    "ObjectId('61bbafc3bebd7b2275d2617b')",
    "ObjectId('61bbb6751b06f1948c798d70')"
  ]
},
{
  "_id": "ObjectId('61bbafc5bebd7b2275d2617f')",
  "filmName": "Spiderman No Way Home",
  "cinemas": [
    "ObjectId('61bbafc3bebd7b2275d2617b')",
    "ObjectId('61bbb6751b06f1948c798d70')"
  ]
}
```
