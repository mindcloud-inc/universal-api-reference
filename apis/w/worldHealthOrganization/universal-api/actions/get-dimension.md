# World Health Organization: Get Dimension

Retrieves a dimension from the World Health Organization.

```
GET https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/get-dimension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World Health Organization `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/get-dimension?connectionId=$CONNECTION_ID&dimensionCode=REGION" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dimensionCode": "REGION"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/get-dimension?${params}`, {
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
| `dimensionCode` | string | yes | WHO dimension code, such as REGION, COUNTRY, SEX, AGEGROUP, or WORLDBANKINCOMEGROUP. Example: `REGION`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string |  |
| `Title` | string |  |

## Native endpoint

Through the native World Health Organization API, this operation is `GET /DIMENSION/:dimensionCode` (base URL `https://ghoapi.azureedge.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dimension.md) for the provider-specific parameters and requirements.

