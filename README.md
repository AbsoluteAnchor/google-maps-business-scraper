[Google Maps Business Scraper](https://apify.com/salahboussettah/google-maps-business-scraper?fpr=data)

Extract business data from Google Maps search results, including email addresses scraped directly from business websites. Get everything you need for lead generation in one run.

## What data do you get?

| Field | Description |
| --- | --- |
| Business Name | Full name as listed on Google Maps |
| Email | Extracted from the business website (homepage + contact page) |
| Phone | Phone number |
| Address | Full street address |
| Website | Business website URL |
| Rating | Star rating (1-5) |
| Reviews Count | Total number of Google reviews |
| Category | Business category (e.g., "Italian restaurant", "Dentist") |
| Open Now | Whether the business is currently open (true/false) |
| Opening Hours | Full weekly schedule (day by day) |
| Social Media | Facebook, Instagram, Twitter, LinkedIn, TikTok, YouTube links |
| Latitude/Longitude | GPS coordinates |
| Google Maps URL | Direct link to the business on Google Maps |
| Place ID | Google Place ID for API integration |

## How to use

1. Enter your **search query** (e.g., "restaurants", "dentists", "plumbers")
2. Enter the **location** (e.g., "New York", "London", "Tokyo")
3. Set the **maximum number of results** (up to 200)
4. Click **Start**

## Input example

```
{
    "searchQuery": "restaurants",
    "location": "New York",
    "maxResults": 40,
    "language": "en"
}
```

## Output example

```
{
    "name": "Le Bernardin",
    "email": "gifts@le-bernardin.com",
    "phone": "+1 212-554-1515",
    "address": "155 W 51st St, New York, NY 10019, United States",
    "website": "https://www.le-bernardin.com/home",
    "rating": 4.6,
    "reviews_count": 4729,
    "category": "French restaurant",
    "price_level": null,
    "currently_open": false,
    "opening_hours": {
        "Monday": "12 PM - 10 PM",
        "Tuesday": "12 PM - 10 PM",
        "Wednesday": "12 PM - 10 PM",
        "Thursday": "12 PM - 10 PM",
        "Friday": "12 PM - 10:30 PM",
        "Saturday": "5 PM - 10:30 PM",
        "Sunday": "Closed"
    },
    "social_media": {},
    "latitude": 40.7614218,
    "longitude": -73.9817558,
    "google_maps_url": "https://www.google.com/maps/place/Le+Bernardin/...",
    "place_id": "ChIJV7QQ6kdZwokRax4615zpSGU"
}
```

## Use cases

- **Lead generation**: Find businesses in any niche and location, complete with emails and phone numbers for outreach
- **Market research**: Analyze ratings, review counts, and categories across competitors
- **Local SEO**: Audit business listings and compare your clients against competitors
- **Sales prospecting**: Build targeted contact lists with verified business emails
- **Real estate analysis**: Map business density and categories in specific areas

## Supported locations

Works with any location worldwide that Google Maps covers. Just enter the city, region, or country name.

## Language support

Set the `language` parameter to any language code (e.g., "en", "fr", "es", "ar", "de", "ja") to get results in your preferred language.

## How email extraction works

The scraper visits each business's website and scans the homepage and common contact pages (/contact, /contact-us, /about) for email addresses. It filters out generic emails (noreply, mailer-daemon) and tracking pixels to give you real, usable business emails.

## Limitations

- Google Maps typically shows up to 120 results per search query
- Email extraction depends on whether the business has an email listed on their website
- Social media links are only available when businesses have added them to their Google Business Profile
- The "currently open" status reflects the time of scraping