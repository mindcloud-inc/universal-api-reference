# Zoho FSM: List Service Appointments

Retrieves service appointments from Zoho FSM.

```
GET https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-service-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-service-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-service-appointments?${params}`, {
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
| `page` | number | no | Page number to fetch. |
| `perPage` | number | no | Number of records per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$currency_symbol": "string",
      "$editable": true,
      "$inactive": true,
      "Actual_Duration": 1,
      "Actual_End_Date_Time": "2026-05-07T12:00:00.000Z",
      "Actual_Start_Date_Time": "2026-05-07T12:00:00.000Z",
      "Adjustment": 1,
      "Appointment_Date": "2026-05-07T12:00:00.000Z",
      "Asset": "string",
      "Billing_Status": "string",
      "Cancellation_Message": "string",
      "Cancellation_Reason": "string",
      "Cancelled_Or_Terminated_Time": "2026-05-07T12:00:00.000Z",
      "Company": {
        "id": "string",
        "name": "Ava Chen"
      },
      "Contact": {
        "id": "string",
        "name": "Ava Chen"
      },
      "Created_By": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "Created_Time": "2026-05-07T12:00:00.000Z",
      "Currency": "string",
      "Discount": 1,
      "Due_Date": "2026-05-07T12:00:00.000Z",
      "Duration": {
        "actual_duration": 1,
        "appointment_count": 1,
        "scheduled_duration": 1
      },
      "Email": "ava@example.com",
      "Exchange_Rate": 1,
      "id": "string",
      "Invoice_Id": "string",
      "Lead": "string",
      "Mobile": "string",
      "Modified_By": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "Modified_Time": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "Overlapping_Appointments": 1,
      "Owner": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "Phone": "string",
      "Preference": {
        "Preference_Note": "string",
        "Preferred_Date_1": "2026-05-07T12:00:00.000Z",
        "Preferred_Date_2": "2026-05-07T12:00:00.000Z",
        "Preferred_Time": "string"
      },
      "Round_Off": 1,
      "Schedule_Type": "string",
      "Scheduled_Duration": 1,
      "Scheduled_End_Date_Time": "2026-05-07T12:00:00.000Z",
      "Scheduled_Maintenance": "string",
      "Scheduled_Start_Date_Time": "2026-05-07T12:00:00.000Z",
      "Service_Address": {
        "id": "string",
        "name": "Ava Chen",
        "Service_Address_Name": "Ava Chen",
        "Service_City": "string",
        "Service_Country": "string",
        "Service_Google_Geocodedtime": "string",
        "Service_Latitude": 1,
        "Service_Longitude": 1,
        "Service_State": "string",
        "Service_Street_1": "string",
        "Service_Street_2": "string",
        "Service_Zip_Code": "string"
      },
      "Status": "string",
      "Sub_Total": 1,
      "Summary": "string",
      "Tax_Amount": 1,
      "Territory": {
        "id": "string",
        "name": "Ava Chen"
      },
      "Total": 1,
      "Type": "string",
      "User_Lead": "string",
      "Work_Order": {
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$currency_symbol` | string |  |
| `$editable` | boolean |  |
| `$inactive` | boolean |  |
| `Actual_Duration` | number |  |
| `Actual_End_Date_Time` | date |  |
| `Actual_Start_Date_Time` | date |  |
| `Adjustment` | number |  |
| `Appointment_Date` | date |  |
| `Asset` | string |  |
| `Billing_Status` | string |  |
| `Cancellation_Message` | string |  |
| `Cancellation_Reason` | string |  |
| `Cancelled_Or_Terminated_Time` | date |  |
| `Company.id` | string |  |
| `Company.name` | string |  |
| `Contact.id` | string |  |
| `Contact.name` | string |  |
| `Created_By.email` | string |  |
| `Created_By.id` | string |  |
| `Created_By.name` | string |  |
| `Created_Time` | date |  |
| `Currency` | string |  |
| `Discount` | number |  |
| `Due_Date` | date |  |
| `Duration.actual_duration` | number |  |
| `Duration.appointment_count` | number |  |
| `Duration.scheduled_duration` | number |  |
| `Email` | string |  |
| `Exchange_Rate` | number |  |
| `id` | string |  |
| `Invoice_Id` | string |  |
| `Lead` | string |  |
| `Mobile` | string |  |
| `Modified_By.email` | string |  |
| `Modified_By.id` | string |  |
| `Modified_By.name` | string |  |
| `Modified_Time` | date |  |
| `Name` | string |  |
| `Overlapping_Appointments` | number |  |
| `Owner.email` | string |  |
| `Owner.id` | string |  |
| `Owner.name` | string |  |
| `Phone` | string |  |
| `Preference.Preference_Note` | string |  |
| `Preference.Preferred_Date_1` | date |  |
| `Preference.Preferred_Date_2` | date |  |
| `Preference.Preferred_Time` | string |  |
| `Round_Off` | number |  |
| `Schedule_Type` | string |  |
| `Scheduled_Duration` | number |  |
| `Scheduled_End_Date_Time` | date |  |
| `Scheduled_Maintenance` | string |  |
| `Scheduled_Start_Date_Time` | date |  |
| `Service_Address.id` | string |  |
| `Service_Address.name` | string |  |
| `Service_Address.Service_Address_Name` | string |  |
| `Service_Address.Service_City` | string |  |
| `Service_Address.Service_Country` | string |  |
| `Service_Address.Service_Google_Geocodedtime` | string |  |
| `Service_Address.Service_Latitude` | number |  |
| `Service_Address.Service_Longitude` | number |  |
| `Service_Address.Service_State` | string |  |
| `Service_Address.Service_Street_1` | string |  |
| `Service_Address.Service_Street_2` | string |  |
| `Service_Address.Service_Zip_Code` | string |  |
| `Status` | string |  |
| `Sub_Total` | number |  |
| `Summary` | string |  |
| `Tax_Amount` | number |  |
| `Territory.id` | string |  |
| `Territory.name` | string |  |
| `Total` | number |  |
| `Type` | string |  |
| `User_Lead` | string |  |
| `Work_Order.id` | string |  |
| `Work_Order.name` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `GET /Service_Appointments` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-appointments.md) for the provider-specific parameters and requirements.

