# Get company details with ConnectSafely

Retrieve detailed information about a specific LinkedIn company page including full description, specialties, employee count, headquarters location, and industry classification.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/companies/details`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get company details](https://connectsafely.ai/docs/api/linkedin-search/post-search-companies-details-get-company-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `companyId` | body | `string` | yes | LinkedIn company ID from search results or company page URL |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `company` | `object` | Detailed company information |
| `company.id` | `string` | LinkedIn company ID |
| `company.name` | `string` | Company name |
| `company.universalName` | `string` | Company URL slug |
| `company.tagline` | `string` | Company tagline |
| `company.description` | `string` | Full company description |
| `company.websiteUrl` | `string` | Company website URL |
| `company.phone` | `string` | Company phone number |
| `company.companyType` | `string` | Type of company (COMPANY, EDUCATIONAL, etc.) |
| `company.headquarters` | `object` | Headquarters location details |
| `company.employeeRange` | `object` |  |
| `company.employeeRange.start` | `number` | Minimum employees |
| `company.employeeRange.end` | `number` | Maximum employees (null for 10001+) |
| `company.staffCount` | `number` | Actual staff count on LinkedIn |
| `company.specialities` | `array` | Company specialties and focus areas |
| `company.logoUrl` | `string` | Company logo URL |
| `company.coverImageUrl` | `string` | Company cover image URL |
| `company.linkedinUrl` | `string` | Direct URL to company page |
| `company.isActive` | `boolean` | Whether the company page is active |
| `company.isVerified` | `boolean` | Whether the company is verified |

### Example response

```json
{
  "success": true,
  "company": {
    "id": "1441",
    "name": "Google",
    "universalName": "google",
    "tagline": null,
    "description": "A problem isn't truly solved until it's solved for all...",
    "websiteUrl": "https://goo.gle/3DLEokh",
    "phone": null,
    "companyType": "COMPANY",
    "headquarters": {},
    "employeeRange": {
      "start": 10001,
      "end": null
    },
    "staffCount": 334483,
    "specialities": [
      "search",
      "ads",
      "mobile",
      "android",
      "machine learning"
    ],
    "logoUrl": "https://media.licdn.com/dms/image/.../google_logo",
    "coverImageUrl": "https://media.licdn.com/dms/image/.../google_cover",
    "linkedinUrl": "https://www.linkedin.com/company/google/",
    "isActive": true,
    "isVerified": false
  }
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
