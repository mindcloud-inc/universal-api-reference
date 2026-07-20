# Congress.gov: Get Amendment

Retrieves an amendment from Congress.gov.

```
GET https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-amendment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Congress.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-amendment?connectionId=$CONNECTION_ID&congress=118&amendmentType=samdt&amendmentNumber=2137" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "congress": "118",
  "amendmentType": "samdt",
  "amendmentNumber": "2137"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-amendment?${params}`, {
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
| `congress` | number | yes | The congress number. For example, 118. Example: `118`. |
| `amendmentType` | string | yes | The amendment type. Values include hamdt, samdt, or suamdt. Example: `samdt`. |
| `amendmentNumber` | number | yes | The amendment's assigned number. For example, 2137. Example: `2137`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amendment": {},
      "request": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amendment` | object |  |
| `request` | object |  |

## Native endpoint

Through the native Congress.gov API, this operation is `GET /amendment/:congress/:amendmentType/:amendmentNumber` (base URL `https://api.congress.gov/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-amendment.md) for the provider-specific parameters and requirements.

