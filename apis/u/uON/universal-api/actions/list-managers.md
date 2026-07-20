# U-ON: List Managers

Retrieves manager records stored in U-ON.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-managers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-managers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-managers?${params}`, {
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
| `office_id` | number | no | ID офиса (см. метод /company-office) / Office ID (see method /company-office) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "address": "string",
      "address_juridical": "string",
      "any_new_lead_notification": 1,
      "any_new_request_notification": 1,
      "bcard_id": "string",
      "bcard_number": "string",
      "bcard_value": "string",
      "cabinet_created": 1,
      "cabinet_created_date": "string",
      "deleted": 1,
      "delivery_subscription": 1,
      "global_u_id": 1,
      "ip_internal_number": "string",
      "labels": "string",
      "manager_id": 1,
      "my_new_lead_notification": 1,
      "my_new_request_notification": 1,
      "nationality": "string",
      "nationality_id": "string",
      "office_id": "string",
      "role_id": 1,
      "source_id": 1,
      "status_id": 1,
      "timezone": "string",
      "tourist_kind": "string",
      "u_birthday": "string",
      "u_birthday_certificate": "string",
      "u_birthday_certificate_given": "string",
      "u_birthday_certificate_organization": "string",
      "u_birthday_place": "string",
      "u_company": "string",
      "u_date_update": "string",
      "u_discount": "string",
      "u_email": "ava@example.com",
      "u_fax": "string",
      "u_finance_bank": "string",
      "u_finance_bik": "string",
      "u_finance_ks": "string",
      "u_finance_okpo": "string",
      "u_finance_rs": "string",
      "u_id": 1,
      "u_image": "string",
      "u_inn": "string",
      "u_instagram": "string",
      "u_kpp": "string",
      "u_manager_status": 1,
      "u_max": "string",
      "u_name": "Ava Chen",
      "u_name_en": "Ava Chen",
      "u_note": "string",
      "u_ogrn": "string",
      "u_okved": "string",
      "u_passport_code": "string",
      "u_passport_date": "string",
      "u_passport_number": "string",
      "u_passport_taken": "string",
      "u_phone": "string",
      "u_phone_home": "string",
      "u_phone_mobile": "string",
      "u_position": "string",
      "u_sex": 1,
      "u_sname": "Ava Chen",
      "u_social_fb": "string",
      "u_social_ok": "string",
      "u_social_vk": "string",
      "u_surname": "Ava Chen",
      "u_surname_en": "Ava Chen",
      "u_telegram": "string",
      "u_type": 1,
      "u_viber": "string",
      "u_whatsapp": "string",
      "u_zagran_expire": "string",
      "u_zagran_given": "string",
      "u_zagran_number": "string",
      "u_zagran_organization": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `address` | string |  |
| `address_juridical` | string |  |
| `any_new_lead_notification` | number |  |
| `any_new_request_notification` | number |  |
| `bcard_id` | string |  |
| `bcard_number` | string |  |
| `bcard_value` | string |  |
| `cabinet_created` | number |  |
| `cabinet_created_date` | string |  |
| `deleted` | number |  |
| `delivery_subscription` | number |  |
| `global_u_id` | number |  |
| `ip_internal_number` | string |  |
| `labels` | string |  |
| `manager_id` | number |  |
| `my_new_lead_notification` | number |  |
| `my_new_request_notification` | number |  |
| `nationality` | string |  |
| `nationality_id` | string |  |
| `office_id` | string |  |
| `role_id` | number |  |
| `source_id` | number |  |
| `status_id` | number |  |
| `timezone` | string |  |
| `tourist_kind` | string |  |
| `u_birthday` | string |  |
| `u_birthday_certificate` | string |  |
| `u_birthday_certificate_given` | string |  |
| `u_birthday_certificate_organization` | string |  |
| `u_birthday_place` | string |  |
| `u_company` | string |  |
| `u_date_update` | string |  |
| `u_discount` | string |  |
| `u_email` | string |  |
| `u_fax` | string |  |
| `u_finance_bank` | string |  |
| `u_finance_bik` | string |  |
| `u_finance_ks` | string |  |
| `u_finance_okpo` | string |  |
| `u_finance_rs` | string |  |
| `u_id` | number |  |
| `u_image` | string |  |
| `u_inn` | string |  |
| `u_instagram` | string |  |
| `u_kpp` | string |  |
| `u_manager_status` | number |  |
| `u_max` | string |  |
| `u_name` | string |  |
| `u_name_en` | string |  |
| `u_note` | string |  |
| `u_ogrn` | string |  |
| `u_okved` | string |  |
| `u_passport_code` | string |  |
| `u_passport_date` | string |  |
| `u_passport_number` | string |  |
| `u_passport_taken` | string |  |
| `u_phone` | string |  |
| `u_phone_home` | string |  |
| `u_phone_mobile` | string |  |
| `u_position` | string |  |
| `u_sex` | number |  |
| `u_sname` | string |  |
| `u_social_fb` | string |  |
| `u_social_ok` | string |  |
| `u_social_vk` | string |  |
| `u_surname` | string |  |
| `u_surname_en` | string |  |
| `u_telegram` | string |  |
| `u_type` | number |  |
| `u_viber` | string |  |
| `u_whatsapp` | string |  |
| `u_zagran_expire` | string |  |
| `u_zagran_given` | string |  |
| `u_zagran_number` | string |  |
| `u_zagran_organization` | string |  |

## Native endpoint

Through the native U-ON API, this operation is `GET /manager.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-managers.md) for the provider-specific parameters and requirements.

