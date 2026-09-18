# Reaven Product Scraper

Production Finds scraper for [Reaven](https://www.reaven.co/en/).

- Source: `scraper-reaven`
- Schedule: `43 21 * * 3` UTC (Wednesdays)
- Currency: EUR
- Gender default: Men
- Embeddings: local SigLIP `google/siglip-base-patch16-384`
- Secrets: `SUPABASE_URL`, `SUPABASE_KEY`
- Catalog crawl: store-wide `/en/products.json?limit=250&page=N` (~88 products)
- Upsert batch size: 5 with single-row fallback; never sends `embedding_version`
