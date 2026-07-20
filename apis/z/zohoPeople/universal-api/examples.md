# Zoho People Universal API Examples

These examples use the MindCloud API key and Zoho People connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organization Info

Retrieves organization details from Zoho People.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-organization-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-organization-info?${params}`, {
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
      "address": {
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string"
      },
      "contactMailId": "string",
      "contactNumber": "string",
      "contactPerson": "string",
      "dateFormat": "string",
      "timeFormat": "string",
      "timeZone": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Organization Info action reference](actions/get-organization-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoPeople/latest/actions/get-organization-info).

## Add Attendance Entries

Creates attendance entries in Zoho People.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/add-attendance-entries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "punchDetails": "string",
  "datetimeFormat": "yyyy-MM-dd HH:mm:ss"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/add-attendance-entries', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "punchDetails": "string",
    "datetimeFormat": "yyyy-MM-dd HH:mm:ss"
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
      "data": {
        "empty_employee_ids": [
          "string"
        ],
        "error_information": [
          {}
        ],
        "maximum_entry_date": "string",
        "minimmun_entry_date": "string",
        "skipped_empolyee_info": [
          {}
        ],
        "success_count": 1,
        "total_count": 1
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Attendance Entries action reference](actions/add-attendance-entries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoPeople/latest/actions/add-attendance-entries).
