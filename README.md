# Leboncoin-API
Complete API leboncoin.fr (immobilier, locations, petites annonces) to Scrap Data with Free Version

https://rapidapi.com/schmidtfischer2/api/lbc-complete-api

### GET /cookie_datadome
Returns a valid Datadome cookie to insert into your requests to avoid deadlocks

### POST /search_ads
search ads with filter

#### JSON BODY
```
{
    "filters": {
        "category": {
            "id": "34"
        },
        "enums": {
            "ad_type": [
                "offer"
            ]
        },
        "keywords": {
            "text": "a"
        },
        "location": {
            "locations": [
                {
                    "locationType": "region",
                    "label": "",
                    "region_id": "12"
                }
            ]
        },
        "ranges": {}
    },
    "limit": 35,
    "limit_alu": 3,
    "sort_order": "desc",
    "offset": 0,
    "sort_by": "time",
    "owner_type": "pro"
}
```

### GET /location_auto_complete/{text}
auto_complete specifique address

### GET /phone_number/{list_id}
get phone_number of ad

### GET /single_ad/{list_id}
get information detail about ad
