# Freshworks CRM Universal API Examples

These examples use the MindCloud API key and Freshworks CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contact Fields

Retrieves contact fields from Freshworks CRM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-contact-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-contact-fields?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {
          "actionable": true,
          "base_model": "string",
          "choices": [
            {
              "id": "string",
              "position": 1,
              "value": "string"
            }
          ],
          "default": true,
          "id": 1,
          "label": "string",
          "name": "Ava Chen",
          "position": 1,
          "quick_add_position": 1,
          "required": true,
          "type": "string",
          "visible": true
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Contact Fields action reference](actions/list-contact-fields.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freshworksCRM/latest/actions/list-contact-fields).

## Add Contacts To List

Adds contacts to a list in Freshworks CRM.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/add-contacts-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "ids[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/add-contacts-to-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "ids[]": [1]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Contacts To List action reference](actions/add-contacts-to-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/freshworksCRM/latest/actions/add-contacts-to-list).
