# Apple News and Music: Native API Reference

A consolidated summary of Apple News and Music's API configuration and 65 documented operations, with links to official documentation.

- **Official docs:** https://performance-partners.apple.com/search-api
- **API base URL:** `https://itunes.apple.com`

## Authentication

### No Auth

Apple Developer News RSS, Apple Newsroom RSS, and the public iTunes Search and Lookup API do not require authentication for this connector path.

This API does not require request authentication.

[Official authentication documentation](https://performance-partners.apple.com/search-api)

## Endpoints (65 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Apple Developer News](actions/list-apple-developer-news.md) | `GET https://developer.apple.com/news/rss/news.rss` | [docs](https://developer.apple.com/news/rss/news.rss) |
| [List Apple Developer Releases](actions/list-apple-developer-releases.md) | `GET https://developer.apple.com/news/releases/rss/releases.rss` | [docs](https://developer.apple.com/news/releases/rss/releases.rss) |
| [List Apple Developer Site Updates](actions/list-apple-developer-site-updates.md) | `GET https://developer.apple.com/news/site-updates/rss/site-updates.rss` | [docs](https://developer.apple.com/news/site-updates/rss/site-updates.rss) |
| [List Apple Newsroom Articles](actions/list-apple-newsroom-articles.md) | `GET https://www.apple.com/newsroom/rss-feed.rss` | [docs](https://www.apple.com/newsroom/rss-feed.rss) |
| [List Top Albums (Top 10)](actions/list-top-albums-top10.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/10/albums.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Albums (Top 100)](actions/list-top-albums-top100.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/100/albums.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Albums (Top 25)](actions/list-top-albums-top25.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/25/albums.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Albums (Top 50)](actions/list-top-albums-top50.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/50/albums.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Audiobooks (Top 10)](actions/list-top-audiobooks-top10.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/audio-books/top/10/audio-books.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Audiobooks (Top 100)](actions/list-top-audiobooks-top100.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/audio-books/top/100/audio-books.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Audiobooks (Top 25)](actions/list-top-audiobooks-top25.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/audio-books/top/25/audio-books.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Audiobooks (Top 50)](actions/list-top-audiobooks-top50.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/audio-books/top/50/audio-books.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Free Apps (Top 10)](actions/list-top-free-apps-top10.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/apps/top-free/10/apps.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Free Apps (Top 100)](actions/list-top-free-apps-top100.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/apps/top-free/100/apps.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Free Apps (Top 25)](actions/list-top-free-apps-top25.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/apps/top-free/25/apps.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Free Apps (Top 50)](actions/list-top-free-apps-top50.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/apps/top-free/50/apps.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Free Books (Top 10)](actions/list-top-free-books-top10.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/books/top-free/10/books.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Free Books (Top 100)](actions/list-top-free-books-top100.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/books/top-free/100/books.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Free Books (Top 25)](actions/list-top-free-books-top25.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/books/top-free/25/books.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Free Books (Top 50)](actions/list-top-free-books-top50.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/books/top-free/50/books.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Music Videos (Top 10)](actions/list-top-music-videos-top10.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/10/music-videos.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Music Videos (Top 100)](actions/list-top-music-videos-top100.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/100/music-videos.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Music Videos (Top 25)](actions/list-top-music-videos-top25.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/25/music-videos.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Music Videos (Top 50)](actions/list-top-music-videos-top50.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/50/music-videos.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Paid Apps (Top 10)](actions/list-top-paid-apps-top10.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/apps/top-paid/10/apps.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Paid Apps (Top 100)](actions/list-top-paid-apps-top100.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/apps/top-paid/100/apps.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Paid Apps (Top 25)](actions/list-top-paid-apps-top25.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/apps/top-paid/25/apps.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Paid Apps (Top 50)](actions/list-top-paid-apps-top50.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/apps/top-paid/50/apps.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Paid Books (Top 10)](actions/list-top-paid-books-top10.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/books/top-paid/10/books.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Paid Books (Top 100)](actions/list-top-paid-books-top100.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/books/top-paid/100/books.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Paid Books (Top 25)](actions/list-top-paid-books-top25.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/books/top-paid/25/books.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Paid Books (Top 50)](actions/list-top-paid-books-top50.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/books/top-paid/50/books.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Playlists (Top 10)](actions/list-top-playlists-top10.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/10/playlists.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Playlists (Top 100)](actions/list-top-playlists-top100.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/100/playlists.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Playlists (Top 25)](actions/list-top-playlists-top25.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/25/playlists.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Playlists (Top 50)](actions/list-top-playlists-top50.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/50/playlists.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Podcast Episodes (Top 10)](actions/list-top-podcast-episodes-top10.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/podcasts/top/10/podcast-episodes.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Podcast Episodes (Top 100)](actions/list-top-podcast-episodes-top100.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/podcasts/top/100/podcast-episodes.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Podcast Episodes (Top 25)](actions/list-top-podcast-episodes-top25.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/podcasts/top/25/podcast-episodes.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Podcast Episodes (Top 50)](actions/list-top-podcast-episodes-top50.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/podcasts/top/50/podcast-episodes.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Podcasts (Top 10)](actions/list-top-podcasts-top10.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/podcasts/top/10/podcasts.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Podcasts (Top 100)](actions/list-top-podcasts-top100.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/podcasts/top/100/podcasts.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Podcasts (Top 25)](actions/list-top-podcasts-top25.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/podcasts/top/25/podcasts.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Podcasts (Top 50)](actions/list-top-podcasts-top50.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/podcasts/top/50/podcasts.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Songs (Top 10)](actions/list-top-songs-top10.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/10/songs.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Songs (Top 100)](actions/list-top-songs-top100.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/100/songs.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Songs (Top 25)](actions/list-top-songs-top25.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/25/songs.json` | [docs](https://rss.marketingtools.apple.com/) |
| [List Top Songs (Top 50)](actions/list-top-songs-top50.md) | `GET https://rss.marketingtools.apple.com/api/v2/us/music/most-played/50/songs.json` | [docs](https://rss.marketingtools.apple.com/) |
| [Lookup Album by UPC](actions/lookup-album-by-upc.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup Album Tracks by Collection ID](actions/lookup-album-tracks-by-collection-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup AMG Artist Albums](actions/lookup-amg-artist-albums.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup App by App Store ID](actions/lookup-app-by-app-store-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup App by Bundle ID](actions/lookup-app-by-bundle-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup Artist Albums by Artist ID](actions/lookup-artist-albums-by-artist-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup Artist Music Videos by Artist ID](actions/lookup-artist-music-videos-by-artist-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup Artist Songs by Artist ID](actions/lookup-artist-songs-by-artist-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup Audiobook by Collection ID](actions/lookup-audiobook-by-collection-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup Author Ebooks by Artist ID](actions/lookup-author-ebooks-by-artist-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup Book by ISBN](actions/lookup-book-by-isbn.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup by AMG Artist ID](actions/lookup-by-amg-artist-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup Catalog Item by iTunes ID](actions/lookup-catalog-item-by-itunes-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup Ebook by Apple ID](actions/lookup-ebook-by-apple-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup Music Video by Track ID](actions/lookup-music-video-by-track-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup Podcast Episodes by Podcast ID](actions/lookup-podcast-episodes-by-podcast-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
| [Lookup Song by Track ID](actions/lookup-song-by-track-id.md) | `GET https://itunes.apple.com/lookup` | [docs](https://performance-partners.apple.com/search-api) |
