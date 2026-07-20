# <img src="https://images.mindcloud.co/apps/icons/pantry_1778173076845.png" alt="Pantry logo" width="28" height="28"> Pantry: Universal API

Store and manage JSON baskets with Pantry

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pantry/latest
- **Category:** IT Operations / Database
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getpantry.cloud
- **Vendor API docs:** https://documenter.getpostman.com/view/3281832/SzmZeMLC

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Pantry Details](actions/get-pantry-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pantry/latest/actions/get-pantry-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Basket

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Replace Basket](actions/create-or-replace-basket.md) | POST | Creates or replaces a basket in Pantry. |
| [Delete Basket](actions/delete-basket.md) | DELETE | Deletes an existing basket from Pantry. |
| [Get Basket Contents](actions/get-basket-contents.md) | GET | Retrieves basket contents from Pantry. |
| [Update Basket Contents](actions/update-basket-contents.md) | PUT | Updates basket contents in Pantry. |

### Pantry

| Action | Method | Description |
| --- | --- | --- |
| [Get Pantry Details](actions/get-pantry-details.md) | GET | Retrieves pantry details from Pantry. |
| [Update Pantry Details](actions/update-pantry-details.md) | PUT | Updates pantry details in Pantry. |

### Public Basket

| Action | Method | Description |
| --- | --- | --- |
| [Get Public Basket Contents](actions/get-public-basket-contents.md) | GET | Retrieves public basket contents from Pantry. |
| [Get Public Basket ID](actions/get-public-basket-id.md) | GET | Retrieves a public basket ID from Pantry. |

