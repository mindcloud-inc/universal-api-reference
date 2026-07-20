# Rentman Universal API Examples

These examples use the MindCloud API key and Rentman connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-contacts?${params}`, {
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
      "accounting_code": "string",
      "admin_contactperson": "string",
      "bank_account": "string",
      "bic": "string",
      "code": "string",
      "commerce_code": "string",
      "contact_warning": "string",
      "country": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "custom": {},
      "default_person": "string",
      "discount_crew": 1,
      "discount_rental": 1,
      "discount_sale": 1,
      "discount_subrent": 1,
      "discount_total": 1,
      "discount_transport": 1,
      "displayname": "Ava Chen",
      "distance": 1,
      "email_1": "ava@example.com",
      "email_2": "ava@example.com",
      "ext_name_line": "Ava Chen",
      "firstname": "Ava",
      "fiscal_code": "string",
      "folder": "string",
      "gender": "string",
      "id": 1,
      "image": "string",
      "invoice_city": "string",
      "invoice_country": "string",
      "invoice_district": "string",
      "invoice_extra_address_line": "string",
      "invoice_number": "string",
      "invoice_postalcode": "string",
      "invoice_state": "string",
      "invoice_street": "string",
      "invoice_unit_number": "string",
      "latitude": 1,
      "longitude": 1,
      "mailing_city": "string",
      "mailing_country": "string",
      "mailing_district": "string",
      "mailing_extra_address_line": "string",
      "mailing_number": "string",
      "mailing_postalcode": "string",
      "mailing_state": "string",
      "mailing_street": "string",
      "mailing_unit_number": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "phone_1": "string",
      "phone_2": "string",
      "projectnote": "string",
      "projectnote_title": "string",
      "purchase_number": "string",
      "surfix": "string",
      "surname": "Ava Chen",
      "tags": "string",
      "travel_time": 1,
      "type": "string",
      "updateHash": "string",
      "VAT_code": "string",
      "vendor_accounting_code": "string",
      "visit_city": "string",
      "visit_district": "string",
      "visit_extra_address_line": "string",
      "visit_number": "string",
      "visit_postalcode": "string",
      "visit_state": "string",
      "visit_street": "string",
      "visit_unit_number": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rentman/latest/actions/list-contacts).

## Create Appointment



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rentman/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "start": "2026-05-07T12:00:00.000Z",
    "end": "2026-05-07T12:00:00.000Z"
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
      "color": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "displayname": "Ava Chen",
      "end": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_plannable": true,
      "is_public": true,
      "location": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "recurrence_enddate": "2026-05-07T12:00:00.000Z",
      "recurrence_group": 1,
      "recurrence_interval": 1,
      "recurrence_interval_unit": "string",
      "recurrence_weekdays": "string",
      "remark": "string",
      "start": "2026-05-07T12:00:00.000Z",
      "synchronisation_uri": "string",
      "synchronization_id": "string",
      "updateHash": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Appointment action reference](actions/create-appointment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rentman/latest/actions/create-appointment).
