# Calculate Surplus Lines Taxes with Surplus Lines Tax

## Endpoint

- **Method:** `POST`
- **Path:** `/calculate`
- **Base URL:** `https://api.surpluslinesapi.com/v1`
- **Official documentation:** [Calculate Surplus Lines Taxes](https://surpluslinesapi.com/docs/#calculate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | body | `string` | yes | State name or two-letter abbreviation. |
| `premium` | body | `number` | yes | Premium amount in USD. |
| `effective_date` | body | `date` | no | Historical calculation date in YYYY-MM-DD format. |
| `year` | body | `number` | no | Tax year used for Iowa's phased-down rates. |
| `wet_marine` | body | `boolean` | no | Use Alaska's wet marine tax treatment. |
| `fire_insurance` | body | `boolean` | no | Apply fire insurance rules where supported. |
| `electronic_filing` | body | `boolean` | no | Apply electronic filing rules where supported. |
| `fire_marshal_rate` | body | `number` | no | Fire marshal tax rate as a decimal between 0 and 0.01 for Illinois. |
| `medical_malpractice` | body | `boolean` | no | Apply Puerto Rico medical malpractice exemption. |
| `workers_comp` | body | `boolean` | no | Apply Virginia workers compensation exemption. |
| `new_business` | body | `boolean` | no | Include Oregon's new or renewal policy service charge. |
