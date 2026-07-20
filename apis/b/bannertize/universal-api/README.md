# <img src="https://images.mindcloud.co/apps/icons/bannertize_1782739349166.png" alt="Bannertize logo" width="28" height="28"> Bannertize: Universal API

Generate and retrieve banner images, templates, and set renders from Bannertize.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bannertize/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bannertize.com
- **Vendor API docs:** https://docs.bannertize.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Generate Images via Set](actions/generate-images-via-set.md) | POST | Creates multiple images from a set in Bannertize. |
| [Retrieve Set](actions/retrieve-set.md) | GET | Retrieves a generated set instance from Bannertize. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves current account credits and usage from Bannertize. |

### Creative Assets

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | POST | Creates a new image from a template in Bannertize. |
| [Retrieve Image](actions/retrieve-image.md) | GET | Retrieves a generated image and render status from Bannertize. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a template and its modifications from Bannertize. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Bannertize. |

