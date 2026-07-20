# Connecteam: List Custom Fields

Retrieves all custom fields associated with the account. Optionally, filter the results by categories, names, types, or custom field IDs.

```
GET https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Connecteam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/list-custom-fields?${params}`, {
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
| `customFieldIds` | array<number> | no | Accepts multiple values as an array. |
| `categoryIds` | array<number> | no | Accepts multiple values as an array. |
| `customFieldTypes` | array<string> | no | Accepts multiple values as an array. |
| `customFieldNames` | array<string> | no | Accepts multiple values as an array. |
| `limit` | number | no | Default: `10`. |
| `offset` | number | no | Default: `0`. |
| `sort` | string | no |  |
| `order` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": 1,
      "dropdownOptions": [
        {
          "id": 1,
          "isDeleted": true,
          "isDisabled": true,
          "value": "string"
        }
      ],
      "id": 1,
      "isEditableForAllAdmins": true,
      "isEditableForUsers": true,
      "isMultiSelect": true,
      "isRequired": true,
      "isVisibleToAllAdmins": true,
      "isVisibleToUsers": true,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number |  |
| `dropdownOptions[].id` | number |  |
| `dropdownOptions[].isDeleted` | boolean |  |
| `dropdownOptions[].isDisabled` | boolean |  |
| `dropdownOptions[].value` | string |  |
| `id` | number |  |
| `isEditableForAllAdmins` | boolean |  |
| `isEditableForUsers` | boolean |  |
| `isMultiSelect` | boolean |  |
| `isRequired` | boolean |  |
| `isVisibleToAllAdmins` | boolean |  |
| `isVisibleToUsers` | boolean |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Connecteam API, this operation is `GET /users/v1/custom-fields` (base URL `https://api.connecteam.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-custom-fields.md) for the provider-specific parameters and requirements.

