# lanskyscraper

Scrape information from BLACKED, TUSHY, VIXEN, BLACKED RAW, TUSHY RAW, DEEPER using Node.js and Puppeteer.

# Setup
```
npm install
```

# Usage
```
const scraper = require("./path/to/module");

(async () => {

	// Searches for a specific video by Tushy
	console.log(await scraper.getVideo({ studio: "tushy", id: "a-very-special-anniversary" }, ));
	
	// Returns all videos matching "anal"
    	console.log(await scraper.search({ query: "anal" }));
	
	// Returns all videos featuring Kristen Scott
    	console.log(await scraper.searchStar("Kristen Scott"));
	
	// Returns all Tushy videos featuring Gia Derza
	console.log(await scraper.searchSite({ studio: "tushy", query: "gia derza" }));
});
```

# Details
search, searchStar and searchSite will return a list of items (ListingItem), looking like this:
{
  id,
  title,
  stars,
  rating,
  thumbnail,
  studio
}

getVideo will return a Video with more details:
{
  id,
  title,
  stars,
  description,
  duration,
  date,
  rating,
  pictures,
  studio
}

# Test
```
npm run test
```