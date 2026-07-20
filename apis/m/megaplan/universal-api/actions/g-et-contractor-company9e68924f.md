# Megaplan: List Contractor Company



```
GET https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/g-et-contractor-company9e68924f
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/g-et-contractor-company9e68924f?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/g-et-contractor-company9e68924f?${params}`, {
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
| `filter` | string | no | NO_DESCRIPTION |
| `q` | string | no | NO_DESCRIPTION |
| `pageAfter` | object | no | Загрузить страницу, начиная с переданной сущности. |
| `pageBefore` | object | no | Загрузить страницу строго до переданной сущности. |
| `pageWith` | object | no | Загрузить страницу c наличием переданной сущности. |
| `limit` | number | no | Сколько элементов включать в страницу. |
| `fields` | object | no | Набор дополнительных полей, включённых в список |
| `sortBy[]` | array | no | массив полей сортировки |
| `onlyRequestedFields` | boolean | no | отдавать только перечисленные поля |

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

Through the native Megaplan API, this operation is `GET /contractorCompany` (base URL `https://m60888876.megaplan.ru/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/g-et-contractor-company9e68924f.md) for the provider-specific parameters and requirements.

