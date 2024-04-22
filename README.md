# Craftco Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)


[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

Oxylabs' [Craftco Scraper](https://oxylabs.io/products/scraper-api/web/craftco?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Craftco website effortlessly. This brief guide showcases how Craftco Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Craftco results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Craftco page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://craft.co/sogeti-587'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/craftco-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html><html class=\"no-js\" id=\"craft-site\" lang=\"en\"><head><meta charSet=\"utf-8\"/><meta cont ... </html>",
      "created_at": "2024-02-20 12:34:06",
      "updated_at": "2024-02-20 12:34:12",
      "page": 1,
      "url": "https://craft.co/sogeti-587",
      "job_id": "7165685044202195969",
      "status_code": 200
    }
  ]
}
```
With our Craftco Scraper, you can seamlessly extract public data from any Craftco web page. Gather vital design details, such as dimensional specifications, material details, or assembly instructions, to understand the market and outshine your competitors. If you have any queries, contact our support team through live chat or email us at hello@oxylabs.io.
