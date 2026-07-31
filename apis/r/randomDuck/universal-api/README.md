# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785424329293.png" alt="Random Duck logo" width="28" height="28"> Random Duck: Universal API

Read random duck image metadata, direct duck media, available filenames, and HTTP-status duck images from random-d.uk.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/randomDuck/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://random-d.uk/
- **Vendor API docs:** https://random-d.uk/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Duck GIF by Number](actions/get-duck-gif-by-number.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomDuck/latest/actions/get-duck-gif-by-number?connectionId=$CONNECTION_ID&num=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Duck

| Action | Method | Description |
| --- | --- | --- |
| [Get Random Duck](actions/get-random-duck.md) | GET |  |
| [Get Random Duck (Quack)](actions/get-random-duck-quack.md) | GET |  |

### Duck Inventory

| Action | Method | Description |
| --- | --- | --- |
| [List Available Ducks](actions/list-available-ducks.md) | GET |  |

### Duck Media

| Action | Method | Description |
| --- | --- | --- |
| [Get Duck GIF by Number](actions/get-duck-gif-by-number.md) | GET |  |
| [Get Duck Image by Number](actions/get-duck-image-by-number.md) | GET |  |
| [Get HTTP Status Duck](actions/get-http-status-duck.md) | GET |  |
| [Get Random Duck Image](actions/get-random-duck-image.md) | GET |  |

