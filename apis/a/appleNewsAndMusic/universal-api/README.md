# <img src="https://images.mindcloud.co/apps/icons/apple-news-and-music_1776356903146.png" alt="Apple News and Music logo" width="28" height="28"> Apple News and Music: Universal API

Read Apple Developer news feeds, Apple Newsroom posts, and public Apple media catalog results through Apple’s public RSS surfaces and iTunes Search and Lookup API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/appleNewsAndMusic/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 65
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.apple.com
- **Vendor API docs:** https://performance-partners.apple.com/search-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Lookup Catalog Item by iTunes ID](actions/lookup-catalog-item-by-itunes-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appleNewsAndMusic/latest/actions/lookup-catalog-item-by-itunes-id?connectionId=$CONNECTION_ID&id=e.g.%20909253" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (65)

### Album Track

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Album Tracks by Collection ID](actions/lookup-album-tracks-by-collection-id.md) | GET | Retrieves an album's tracks from Apple's catalog by collection ID. |

### Announcements

| Action | Method | Description |
| --- | --- | --- |
| [List Apple Developer News](actions/list-apple-developer-news.md) | GET | Retrieves Apple Developer news from the official RSS feed. |
| [List Apple Developer Releases](actions/list-apple-developer-releases.md) | GET | Retrieves Apple Developer release announcements from the official RSS feed. |
| [List Apple Developer Site Updates](actions/list-apple-developer-site-updates.md) | GET | Retrieves Apple Developer site updates from the official RSS feed. |
| [List Apple Newsroom Articles](actions/list-apple-newsroom-articles.md) | GET | Retrieves Apple Newsroom articles from the official RSS feed. |

### App

| Action | Method | Description |
| --- | --- | --- |
| [Lookup App by App Store ID](actions/lookup-app-by-app-store-id.md) | GET | Retrieves an app from Apple's catalog by App Store ID. |
| [Lookup App by Bundle ID](actions/lookup-app-by-bundle-id.md) | GET | Retrieves an app from Apple's catalog by bundle ID. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [List Top Free Apps (Top 10)](actions/list-top-free-apps-top10.md) | GET | Retrieves the top 10 free apps from App Store charts. |
| [List Top Free Apps (Top 100)](actions/list-top-free-apps-top100.md) | GET | Retrieves the top 100 free apps from App Store charts. |
| [List Top Free Apps (Top 25)](actions/list-top-free-apps-top25.md) | GET | Retrieves the top 25 free apps from App Store charts. |
| [List Top Free Apps (Top 50)](actions/list-top-free-apps-top50.md) | GET | Retrieves the top 50 free apps from App Store charts. |
| [List Top Paid Apps (Top 10)](actions/list-top-paid-apps-top10.md) | GET | Retrieves the top 10 paid apps from App Store charts. |
| [List Top Paid Apps (Top 100)](actions/list-top-paid-apps-top100.md) | GET | Retrieves the top 100 paid apps from App Store charts. |
| [List Top Paid Apps (Top 25)](actions/list-top-paid-apps-top25.md) | GET | Retrieves the top 25 paid apps from App Store charts. |
| [List Top Paid Apps (Top 50)](actions/list-top-paid-apps-top50.md) | GET | Retrieves the top 50 paid apps from App Store charts. |

### Audiobook

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Audiobook by Collection ID](actions/lookup-audiobook-by-collection-id.md) | GET | Retrieves an audiobook from Apple's catalog by collection ID. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Top Audiobooks (Top 10)](actions/list-top-audiobooks-top10.md) | GET | Retrieves the top 10 audiobooks from Apple Books charts. |
| [List Top Audiobooks (Top 100)](actions/list-top-audiobooks-top100.md) | GET | Retrieves the top 100 audiobooks from Apple Books charts. |
| [List Top Audiobooks (Top 25)](actions/list-top-audiobooks-top25.md) | GET | Retrieves the top 25 audiobooks from Apple Books charts. |
| [List Top Audiobooks (Top 50)](actions/list-top-audiobooks-top50.md) | GET | Retrieves the top 50 audiobooks from Apple Books charts. |
| [List Top Free Books (Top 10)](actions/list-top-free-books-top10.md) | GET | Retrieves the top 10 free books from Apple Books charts. |
| [List Top Free Books (Top 100)](actions/list-top-free-books-top100.md) | GET | Retrieves the top 100 free books from Apple Books charts. |
| [List Top Free Books (Top 25)](actions/list-top-free-books-top25.md) | GET | Retrieves the top 25 free books from Apple Books charts. |
| [List Top Free Books (Top 50)](actions/list-top-free-books-top50.md) | GET | Retrieves the top 50 free books from Apple Books charts. |
| [List Top Paid Books (Top 10)](actions/list-top-paid-books-top10.md) | GET | Retrieves the top 10 paid books from Apple Books charts. |
| [List Top Paid Books (Top 100)](actions/list-top-paid-books-top100.md) | GET | Retrieves the top 100 paid books from Apple Books charts. |
| [List Top Paid Books (Top 25)](actions/list-top-paid-books-top25.md) | GET | Retrieves the top 25 paid books from Apple Books charts. |
| [List Top Paid Books (Top 50)](actions/list-top-paid-books-top50.md) | GET | Retrieves the top 50 paid books from Apple Books charts. |
| [Lookup Author Ebooks by Artist ID](actions/lookup-author-ebooks-by-artist-id.md) | GET | Retrieves an author's ebooks from Apple's catalog by artist ID. |
| [Lookup Book by ISBN](actions/lookup-book-by-isbn.md) | GET | Retrieves a book from Apple's catalog by ISBN. |

### Ebook

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Ebook by Apple ID](actions/lookup-ebook-by-apple-id.md) | GET | Retrieves an ebook from Apple's catalog by Apple ID. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List Top Albums (Top 10)](actions/list-top-albums-top10.md) | GET | Retrieves the top 10 albums from Apple Music charts. |
| [List Top Albums (Top 100)](actions/list-top-albums-top100.md) | GET | Retrieves the top 100 albums from Apple Music charts. |
| [List Top Albums (Top 25)](actions/list-top-albums-top25.md) | GET | Retrieves the top 25 albums from Apple Music charts. |
| [List Top Albums (Top 50)](actions/list-top-albums-top50.md) | GET | Retrieves the top 50 albums from Apple Music charts. |
| [List Top Music Videos (Top 10)](actions/list-top-music-videos-top10.md) | GET | Retrieves the top 10 music videos from Apple Music charts. |
| [List Top Music Videos (Top 100)](actions/list-top-music-videos-top100.md) | GET | Retrieves the top 100 music videos from Apple Music charts. |
| [List Top Music Videos (Top 25)](actions/list-top-music-videos-top25.md) | GET | Retrieves the top 25 music videos from Apple Music charts. |
| [List Top Music Videos (Top 50)](actions/list-top-music-videos-top50.md) | GET | Retrieves the top 50 music videos from Apple Music charts. |
| [List Top Playlists (Top 10)](actions/list-top-playlists-top10.md) | GET | Retrieves the top 10 playlists from Apple Music charts. |
| [List Top Playlists (Top 100)](actions/list-top-playlists-top100.md) | GET | Retrieves the top 100 playlists from Apple Music charts. |
| [List Top Playlists (Top 25)](actions/list-top-playlists-top25.md) | GET | Retrieves the top 25 playlists from Apple Music charts. |
| [List Top Playlists (Top 50)](actions/list-top-playlists-top50.md) | GET | Retrieves the top 50 playlists from Apple Music charts. |
| [List Top Podcast Episodes (Top 10)](actions/list-top-podcast-episodes-top10.md) | GET | Retrieves the top 10 podcast episodes from Apple Podcasts charts. |
| [List Top Podcast Episodes (Top 100)](actions/list-top-podcast-episodes-top100.md) | GET | Retrieves the top 100 podcast episodes from Apple Podcasts charts. |
| [List Top Podcast Episodes (Top 25)](actions/list-top-podcast-episodes-top25.md) | GET | Retrieves the top 25 podcast episodes from Apple Podcasts charts. |
| [List Top Podcast Episodes (Top 50)](actions/list-top-podcast-episodes-top50.md) | GET | Retrieves the top 50 podcast episodes from Apple Podcasts charts. |
| [List Top Podcasts (Top 10)](actions/list-top-podcasts-top10.md) | GET | Retrieves the top 10 podcasts from Apple Podcasts charts. |
| [List Top Podcasts (Top 100)](actions/list-top-podcasts-top100.md) | GET | Retrieves the top 100 podcasts from Apple Podcasts charts. |
| [List Top Podcasts (Top 25)](actions/list-top-podcasts-top25.md) | GET | Retrieves the top 25 podcasts from Apple Podcasts charts. |
| [List Top Podcasts (Top 50)](actions/list-top-podcasts-top50.md) | GET | Retrieves the top 50 podcasts from Apple Podcasts charts. |
| [List Top Songs (Top 10)](actions/list-top-songs-top10.md) | GET | Retrieves the top 10 songs from Apple Music charts. |
| [List Top Songs (Top 100)](actions/list-top-songs-top100.md) | GET | Retrieves the top 100 songs from Apple Music charts. |
| [List Top Songs (Top 25)](actions/list-top-songs-top25.md) | GET | Retrieves the top 25 songs from Apple Music charts. |
| [List Top Songs (Top 50)](actions/list-top-songs-top50.md) | GET | Retrieves the top 50 songs from Apple Music charts. |
| [Lookup Album by UPC](actions/lookup-album-by-upc.md) | GET | Retrieves an album from Apple's catalog by UPC. |
| [Lookup AMG Artist Albums](actions/lookup-amg-artist-albums.md) | GET | Retrieves an artist's albums from Apple's catalog by AMG artist ID. |
| [Lookup Artist Albums by Artist ID](actions/lookup-artist-albums-by-artist-id.md) | GET | Retrieves an artist's albums from Apple's catalog by artist ID. |
| [Lookup Artist Music Videos by Artist ID](actions/lookup-artist-music-videos-by-artist-id.md) | GET | Retrieves an artist's music videos from Apple's catalog by artist ID. |
| [Lookup Artist Songs by Artist ID](actions/lookup-artist-songs-by-artist-id.md) | GET | Retrieves an artist's songs from Apple's catalog by artist ID. |
| [Lookup by AMG Artist ID](actions/lookup-by-amg-artist-id.md) | GET | Retrieves a catalog item from Apple's catalog by AMG artist ID. |
| [Lookup Catalog Item by iTunes ID](actions/lookup-catalog-item-by-itunes-id.md) | GET | Retrieves a catalog item from Apple's catalog by iTunes ID. |

### Music Video

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Music Video by Track ID](actions/lookup-music-video-by-track-id.md) | GET | Retrieves a music video from Apple's catalog by track ID. |

### Podcast Episode

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Podcast Episodes by Podcast ID](actions/lookup-podcast-episodes-by-podcast-id.md) | GET | Retrieves podcast episodes from Apple's catalog by podcast ID. |

### Song

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Song by Track ID](actions/lookup-song-by-track-id.md) | GET | Retrieves a song from Apple's catalog by track ID. |

