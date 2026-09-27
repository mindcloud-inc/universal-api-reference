# Fetch LinkedIn profile information with ConnectSafely

Retrieve detailed profile information for a LinkedIn member including name, headline, premium status, and profile URNs. Results are cached for 6 hours to reduce API calls. Optionally include geo location details and contact information (email, phone if visible). **Rate limit: 120 unique profiles per day per LinkedIn account (cached requests do not count against limit).**

## Endpoint

- **Method:** `POST`
- **Path:** `/profile`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Fetch LinkedIn profile information](https://connectsafely.ai/docs/api/linkedin-profiles/post-profile-fetch-profile)

## Quota

120 unique profile fetches per day per LinkedIn account. Cached profiles (within 6 hours) do not count against limit.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `profileId` | body | `string` | yes | LinkedIn profile vanity URL slug (the part after linkedin.com/in/, e.g., "john-doe-123") |
| `includeGeoLocation` | body | `boolean` | no | Include detailed geo location data (city, country, coordinates) Default: `False`. |
| `includeContact` | body | `boolean` | no | Include contact info (email, phone) if visible to viewer Default: `False`. |
| `includeExperience` | body | `boolean` | no | Include work experience history Default: `False`. |
| `includeEducation` | body | `boolean` | no | Include education history Default: `False`. |
| `includeSkills` | body | `boolean` | no | Include skills with endorsement counts Default: `False`. |
| `forceRefresh` | body | `boolean` | no | Skip cache and fetch fresh data from LinkedIn. Use sparingly as it counts against rate limit. Default: `False`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` | Whether the request was successful |
| `profileId` | `string` | The requested profile vanity URL slug |
| `accountId` | `string` | LinkedIn account ID used for the request |
| `profile` | `object` | Profile data (empty object if profile not found) |
| `profile.firstName` | `string` | First name |
| `profile.lastName` | `string` | Last name |
| `profile.headline` | `string` | Professional headline |
| `profile.location` | `object` | Basic location details from profile |
| `profile.location.countryCode` | `string` | ISO country code (e.g., "us", "in") |
| `profile.location.postalCode` | `string` | Postal code if available |
| `profile.location.geoLocationName` | `string` | Location name if available |
| `profile.entityUrn` | `string` | Full profile URN (urn:li:fsd_profile:...) |
| `profile.publicIdentifier` | `string` | Public profile ID (URL slug) |
| `profile.profilePicture` | `string` | Profile picture URL (100x100 thumbnail). May be null for some influencer/creator profiles. |
| `profile.isPremium` | `boolean` | Whether user has LinkedIn Premium |
| `profile.isVerified` | `boolean` | Whether profile is verified by LinkedIn |
| `profile.supportsFreeEmail` | `boolean` | Whether you can send free InMail to this user |
| `profile.connectionCount` | `number` | Number of connections |
| `profile.followerCount` | `number` | Number of followers |
| `profile.isConnected` | `boolean` | Whether you are connected with this user |
| `profile.connectionDegree` | `string` | Connection degree: "DISTANCE_1" (1st), "DISTANCE_2" (2nd), "DISTANCE_3" (3rd+), or null if not connected |
| `profile.invitationSent` | `boolean` | Whether you have sent a pending connection invitation |
| `profile.invitationReceived` | `boolean` | Whether you have a pending invitation from this user |
| `profile.geoLocation` | `object` | Detailed geo location (only included when includeGeoLocation=true) |
| `profile.geoLocation.city` | `string` | City name (e.g., "Delhi", "Seattle") |
| `profile.geoLocation.state` | `string` | State/region name (e.g., "Washington", "Delhi") |
| `profile.geoLocation.country` | `string` | Country name (e.g., "India", "United States") |
| `profile.geoLocation.fullLocation` | `string` | Full location string (e.g., "South Delhi, Delhi, India") |
| `profile.geoLocation.birthDate` | `object` | Birth date if publicly available |
| `profile.geoLocation.birthDate.month` | `number` |  |
| `profile.geoLocation.birthDate.day` | `number` |  |
| `profile.geoLocation.birthDate.year` | `number` |  |
| `experience` | `array` | Work experience history (only included when includeExperience=true) |
| `experience[].title` | `string` | Job title |
| `experience[].companyName` | `string` | Company name |
| `experience[].employmentType` | `string` | Employment type (e.g., "Full-time", "Part-time") |
| `experience[].duration` | `string` | Duration at the position |
| `experience[].location` | `string` | Work location |
| `experience[].description` | `string` | Job description |
| `experience[].companyUrl` | `string` | LinkedIn company page URL |
| `experience[].companyLogoUrl` | `string` | Company logo image URL |
| `skills` | `array` | Skills with endorsement counts (only included when includeSkills=true) |
| `skills[].skillId` | `string` | Skill ID |
| `skills[].name` | `string` | Skill name (e.g., "JavaScript", "Project Management") |
| `skills[].endorsementCount` | `number` | Number of endorsements for this skill |
| `skills[].isEndorsed` | `boolean` | Whether you have endorsed this skill |
| `education` | `array` | Education history (only included when includeEducation=true) |
| `education[].schoolName` | `string` | Name of the school or university |
| `education[].degree` | `string` | Degree type (e.g., "Bachelor", "Master", "PhD", "Diploma") |
| `education[].fieldOfStudy` | `string` | Field of study or major |
| `education[].dateRange` | `string` | Date range string (e.g., "2005 – 2008") |
| `education[].startYear` | `string` | Start year |
| `education[].endYear` | `string` | End year (null if ongoing) |
| `education[].grade` | `string` | Grade or GPA if available |
| `education[].activities` | `string` | Activities and societies |
| `education[].description` | `string` | Education description |
| `cached` | `boolean` | Whether the response was served from cache |
| `cachedAt` | `date` | When the profile was cached (only if cached=true) |
| `expiresAt` | `date` | When the cache expires |
| `message` | `string` | Status message |

### Example response

```json
{
  "success": true,
  "profileId": "anandi-devi",
  "accountId": "696ce9e780e0483585e4e553",
  "profile": {
    "firstName": "Anandi",
    "lastName": "Devi",
    "headline": "Go-To-Market (GTM) Engineer @ ConnectSafely | MBA",
    "location": {
      "countryCode": "in",
      "postalCode": null,
      "geoLocationName": null
    },
    "entityUrn": "urn:li:fsd_profile:ACoAAFpqSoMB8vTqRbg4mN_wbabO8w0gjgFu-6o",
    "publicIdentifier": "anandi-devi",
    "profilePicture": "https://media.licdn.com/dms/image/v2/D5603AQF2Iu7GGz-H2A/profile-displayphoto-shrink_100_100/...",
    "isPremium": true,
    "isVerified": true,
    "supportsFreeEmail": true,
    "connectionCount": 958,
    "followerCount": 1243,
    "isConnected": true,
    "connectionDegree": "DISTANCE_1",
    "invitationSent": false,
    "invitationReceived": false,
    "geoLocation": {
      "city": "Delhi",
      "state": null,
      "country": "India",
      "fullLocation": "Delhi, India",
      "birthDate": null
    }
  },
  "message": "Profile information retrieved successfully"
}
```

## Error status codes

`400`, `401`, `429`. Bodies follow the shared `{ success, code, message }` error shape.
