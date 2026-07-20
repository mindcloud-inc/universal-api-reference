# Société.com: Get Officer Mandates

Retrieves officer mandates from Société.com.

```
GET https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/get-officer-mandates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Société.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/get-officer-mandates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/get-officer-mandates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `directorId` | string | no | Officer id returned by Société.com autocomplete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "civilite": "string",
      "comandataires": [
        {}
      ],
      "mandats": [
        {}
      ],
      "nbcomandataires": 1,
      "nbmandats": 1,
      "nom": "string",
      "prenom": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `civilite` | string | Officer salutation returned by the mandate lookup. |
| `comandataires` | array<object> | Co-mandatory records returned by the API. |
| `mandats` | array<object> | Mandate records associated with the officer. |
| `nbcomandataires` | number | Number of co-mandatories returned by the API. |
| `nbmandats` | number | Number of mandates associated with the officer. |
| `nom` | string | Officer last name. |
| `prenom` | string | Officer first name. |

## Native endpoint

Through the native Société.com API, this operation is `GET /mandats/:dirid` (base URL `https://api.societe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-officer-mandates.md) for the provider-specific parameters and requirements.

