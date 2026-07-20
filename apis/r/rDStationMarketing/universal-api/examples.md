# RD Station Marketing Universal API Examples

These examples use the MindCloud API key and RD Station Marketing connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Custom Fields



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-custom-fields?${params}`, {
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
          "apiIdentifier": "string",
          "customField": true,
          "dataType": "string",
          "label": {
            "default": "string"
          },
          "name": {
            "default": "Ava Chen"
          },
          "presentationType": "string",
          "uuid": "string",
          "validationRules": {
            "validOptions": [
              {
                "value": "string"
              }
            ]
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Custom Fields action reference](actions/list-custom-fields.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rDStationMarketing/latest/actions/list-custom-fields).

## Add Leads to Workflow



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/add-leads-to-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "leads[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/add-leads-to-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "leads[]": ["string"]
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
      "leadsAdded": [
        [
          "string"
        ]
      ],
      "leadsNotFound": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Leads to Workflow action reference](actions/add-leads-to-workflow.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rDStationMarketing/latest/actions/add-leads-to-workflow).
