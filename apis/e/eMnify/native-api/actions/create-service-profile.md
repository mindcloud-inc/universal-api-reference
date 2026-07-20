# Create Service Profile with EMnify

Creates a new service profile in EMnify.

## Endpoint

- **Method:** `POST`
- **Path:** `/service_profile`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Create Service Profile](https://docs.emnify.com/developers/api/service-profiles/service-profile-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `name` | body | `string` | yes | Service profile name. |
| `description` | body | `string` | no | Service profile description. |
| `allowed_3g` | body | `boolean` | no | Allow 3G connectivity. |
| `allowed_4g` | body | `boolean` | no | Allow 4G/LTE and LTE-M connectivity. |
| `allowed_nb_iot` | body | `boolean` | no | Allow NB-IoT connectivity. |
| `allowed_nb_iot_geo` | body | `boolean` | no | Allow NB-IoT connectivity over satellite networks. |
| `apply_sms_quota` | body | `boolean` | no | Apply SMS quota limits. |
| `apply_data_quota` | body | `boolean` | no | Apply data quota limits. |
| `retail` | body | `boolean` | no | Retail mode flag. |
| `sms_p2p_int` | body | `boolean` | no | Allow internal person-to-person SMS. |
| `sms_p2p_ext` | body | `boolean` | no | Allow external person-to-person SMS. |
| `prepaid` | body | `boolean` | no | Deprecated prepaid flag. |
| `nipdp` | body | `boolean` | no | Enable NIPDP. |
| `id` | body | `number` | no | Breakout region ID. |
| `id` | body | `number` | no | DNS configuration ID. |
