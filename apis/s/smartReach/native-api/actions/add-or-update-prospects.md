# Add or Update Prospects with SmartReach

Finds prospects in SmartReach, or creates them if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [Add or Update Prospects](https://help.smartreach.io/reference/addprospects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unique_identifier_columns` | query | `string` | no | Comma-separated list of columns to use as unique identifiers to find duplicates. Valid values: email, phone, linkedin_url, company_firstname_lastname. Defaults to "email" if not provided (backward compatible with existing behavior). Note: The order in which you specify columns does not matter. The system will always check for duplicates in this priority order: email, linkedin_url, phone, company_firstname_lastname. Examples:   - "email" - Use only email to find duplicates (default)   - "phone" - Use only phone to find duplicates   - "linkedin_url" - Use only LinkedIn URL to find duplicates   - "email,phone" - Use both email and phone to find duplicates   - "email,phone,linkedin_url,company_firstname_lastname" - Use all four columns |
| `prospects[]` | body | `array<object>` | yes | Each prospect must have at least one unique identifier column: - email, OR - phone_number, OR - linkedin_url, OR - company + first_name + last_name (all three required together) |
