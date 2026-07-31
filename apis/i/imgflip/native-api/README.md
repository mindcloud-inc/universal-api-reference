# Imgflip: Native API Reference

A consolidated summary of Imgflip's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://imgflip.com/api
- **API base URL:** `https://api.imgflip.com`

## Authentication

### Imgflip account

Dedicated Imgflip username and password are submitted only in the form-encoded caption request body; never use a personal account.

### Credentials

- **Username:** `username` · required · Dedicated Imgflip API account username.
- **Password:** `password` · required · Dedicated Imgflip API account password.

[Official authentication documentation](https://imgflip.com/api)

## API conventions

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Caption Image](actions/caption-image.md) | `POST /caption_image` | [docs](https://imgflip.com/api) |
| [List Popular Memes](actions/list-popular-memes.md) | `GET /get_memes` | [docs](https://imgflip.com/api) |
