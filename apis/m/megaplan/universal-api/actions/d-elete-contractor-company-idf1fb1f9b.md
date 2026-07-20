# Megaplan: Delete Contractor Company



```
DELETE https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/d-elete-contractor-company-idf1fb1f9b
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/d-elete-contractor-company-idf1fb1f9b?connectionId=$CONNECTION_ID&id=string&id=1&body=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "id": "1",
  "body": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/d-elete-contractor-company-idf1fb1f9b?${params}`, {
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
| `id` | string | yes | Path parameter from Megaplan RAML. |
| `id` | number | yes | Идентификатор контрагента |
| `body` | object | yes | Request body. RAML type: DeleteActionRequest |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "data": {},
      "id": "string",
      "meta": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | Megaplan object type when present. |
| `data` | object | Megaplan response data. |
| `id` | string | Megaplan entity identifier when present. |
| `meta` | object | Megaplan response metadata. |
| `success` | boolean | Operation success indicator when present. |

## Native endpoint

Through the native Megaplan API, this operation is `DELETE /contractorCompany/:id` (base URL `https://m60888876.megaplan.ru/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/d-elete-contractor-company-idf1fb1f9b.md) for the provider-specific parameters and requirements.

