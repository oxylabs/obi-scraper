# Obi Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Obi Scraper](https://oxylabs.io/products/scraper-api/ecommerce/obi?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Obi website effortlessly. This brief guide showcases how Obi Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Obi results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Obi page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.obi.pl/kabiny-brodziki-i-akcesoria/kabiny-prysznicowe/c/1226'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/obi-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><!--[if lt IE 7]><html lang=\"pl-PL\" class=\"ie6 no-js\"><![endif]--><!--[if IE 7]><html ... </html>",
      "created_at": "2024-02-20 12:44:29",
      "updated_at": "2024-02-20 12:44:31",
      "page": 1,
      "url": "https://www.obi.pl/kabiny-brodziki-i-akcesoria/kabiny-prysznicowe/c/1226",
      "job_id": "7165687656817393665",
      "status_code": 200
    }
  ]
}
```
With our Obi Scraper, you can seamlessly pull out public data from any Obi webpage. Gather the necessary architectural design information, such as blueprint details, construction material specifications, or project timelines, to stay abreast with the latest industry trends and outperform your competition. If you need any clarification, connect with our support team using our live chat option or email us at hello@oxylabs.io.