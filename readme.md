# Art Basel Gallery Scraper

Get the details of galleries on [Art Basel](https://www.artbasel.com/) and write them into an excel sheet.

## Usage

1. Install dependencies

   ```bash
   pip install -r requirements.txt
   ```

2. run `get_all_galleries.py`

## Fetched Information

https://www.artbasel.com/msvc/v1/artcatalog/gallery/items?limit=36&offset=0&sortBy=sortingName&statuses=102900000
- format: json
- content: gallery list
  - gallery id

https://www.artbasel.com/catalog/gallery/[gallery id]
- format: html
- content: There's a json object called "pageMetaInfo" contained in `<scripts id="__NEXT_DATA__">`
  - pageMetaInfo
    - format: json
    - content: gallery detail
      - displayName
      - description
      - accountId
      - website
      - emailAddress
      - directors
      - addresses

https://www.artbasel.com/msvc/v1/exhibitorprofile/items/ba168459-e063-e211-b62e-00155d35011a/exhibitions?limit=3
- format: json
- content: exibitions

