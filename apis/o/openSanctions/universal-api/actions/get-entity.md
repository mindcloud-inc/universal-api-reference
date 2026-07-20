# OpenSanctions: Get Entity



```
GET https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/get-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSanctions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/get-entity?connectionId=$CONNECTION_ID&entity_id=Q7747" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entity_id": "Q7747"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/get-entity?${params}`, {
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
| `entity_id` | string | yes | ID of the entity to retrieve. OpenSanctions documents Q7747 as an example entity ID. Default: `Q7747`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nested` | boolean | no | Include adjacent entities such as addresses, family, passport, sanction, and associated entities in the response. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "caption": "string",
      "datasets": [
        "string"
      ],
      "firstSeen": "string",
      "id": "string",
      "lastChange": "string",
      "lastSeen": "string",
      "properties": {
        "address": [
          "string"
        ],
        "addressEntity": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "city": [
                "string"
              ],
              "country": [
                "string"
              ],
              "full": [
                "string"
              ],
              "street": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "alias": [
          "string"
        ],
        "associations": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "associate": [
                "string"
              ],
              "person": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "address": [
                      "string"
                    ],
                    "addressEntity": [
                      "string"
                    ],
                    "alias": [
                      "string"
                    ],
                    "birthCountry": [
                      "string"
                    ],
                    "birthDate": [
                      "string"
                    ],
                    "birthPlace": [
                      "string"
                    ],
                    "citizenship": [
                      "string"
                    ],
                    "country": [
                      "string"
                    ],
                    "createdAt": [
                      "string"
                    ],
                    "education": [
                      "string"
                    ],
                    "fatherName": [
                      "Ava Chen"
                    ],
                    "firstName": [
                      "Ava"
                    ],
                    "gender": [
                      "string"
                    ],
                    "innCode": [
                      "string"
                    ],
                    "lastName": [
                      "Chen"
                    ],
                    "middleName": [
                      "Ava Chen"
                    ],
                    "modifiedAt": [
                      "string"
                    ],
                    "name": [
                      "Ava Chen"
                    ],
                    "nationality": [
                      "string"
                    ],
                    "notes": [
                      "string"
                    ],
                    "position": [
                      "string"
                    ],
                    "programId": [
                      "string"
                    ],
                    "sourceUrl": [
                      "https://example.com"
                    ],
                    "topics": [
                      "string"
                    ],
                    "uniqueEntityId": [
                      "string"
                    ],
                    "wikidataId": [
                      "string"
                    ],
                    "wikipediaUrl": [
                      "https://example.com"
                    ]
                  },
                  "referents": [
                    "string"
                  ],
                  "schema": "string",
                  "target": true
                }
              ],
              "relationship": [
                "string"
              ],
              "sourceUrl": [
                "https://example.com"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "birthCountry": [
          "string"
        ],
        "birthDate": [
          "string"
        ],
        "birthPlace": [
          "string"
        ],
        "citizenship": [
          "string"
        ],
        "classification": [
          "string"
        ],
        "country": [
          "string"
        ],
        "createdAt": [
          "string"
        ],
        "description": [
          "string"
        ],
        "documentedBy": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "date": [
                "string"
              ],
              "document": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "publishedAt": [
                      "string"
                    ],
                    "sourceUrl": [
                      "https://example.com"
                    ],
                    "title": [
                      "string"
                    ]
                  },
                  "schema": "string",
                  "target": true
                }
              ],
              "entity": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "education": [
          "string"
        ],
        "ethnicity": [
          "string"
        ],
        "familyPerson": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "person": [
                "string"
              ],
              "relationship": [
                "string"
              ],
              "relative": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "alias": [
                      "string"
                    ],
                    "birthDate": [
                      "string"
                    ],
                    "birthPlace": [
                      "string"
                    ],
                    "citizenship": [
                      "string"
                    ],
                    "firstName": [
                      "Ava"
                    ],
                    "gender": [
                      "string"
                    ],
                    "lastName": [
                      "Chen"
                    ],
                    "name": [
                      "Ava Chen"
                    ],
                    "notes": [
                      "string"
                    ],
                    "topics": [
                      "string"
                    ],
                    "weakAlias": [
                      "string"
                    ],
                    "wikidataId": [
                      "string"
                    ],
                    "wikipediaUrl": [
                      "https://example.com"
                    ]
                  },
                  "schema": "string",
                  "target": true
                }
              ],
              "sourceUrl": [
                "https://example.com"
              ]
            },
            "referents": [
              "string"
            ],
            "schema": "string",
            "target": true
          }
        ],
        "familyRelative": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "person": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "address": [
                      "string"
                    ],
                    "alias": [
                      "string"
                    ],
                    "birthCountry": [
                      "string"
                    ],
                    "birthDate": [
                      "string"
                    ],
                    "birthPlace": [
                      "string"
                    ],
                    "citizenship": [
                      "string"
                    ],
                    "country": [
                      "string"
                    ],
                    "createdAt": [
                      "string"
                    ],
                    "education": [
                      "string"
                    ],
                    "fatherName": [
                      "Ava Chen"
                    ],
                    "firstName": [
                      "Ava"
                    ],
                    "gender": [
                      "string"
                    ],
                    "idNumber": [
                      "string"
                    ],
                    "innCode": [
                      "string"
                    ],
                    "lastName": [
                      "Chen"
                    ],
                    "middleName": [
                      "Ava Chen"
                    ],
                    "modifiedAt": [
                      "string"
                    ],
                    "name": [
                      "Ava Chen"
                    ],
                    "nationality": [
                      "string"
                    ],
                    "notes": [
                      "string"
                    ],
                    "position": [
                      "string"
                    ],
                    "programId": [
                      "string"
                    ],
                    "sourceUrl": [
                      "https://example.com"
                    ],
                    "taxNumber": [
                      "string"
                    ],
                    "topics": [
                      "string"
                    ],
                    "uniqueEntityId": [
                      "string"
                    ],
                    "wikidataId": [
                      "string"
                    ],
                    "wikipediaUrl": [
                      "https://example.com"
                    ]
                  },
                  "referents": [
                    "string"
                  ],
                  "schema": "string",
                  "target": true
                }
              ],
              "relationship": [
                "string"
              ],
              "relative": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "fatherName": [
          "Ava Chen"
        ],
        "firstName": [
          "Ava"
        ],
        "gender": [
          "string"
        ],
        "identification": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "holder": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "lastName": [
          "Chen"
        ],
        "membershipMember": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "member": [
                "string"
              ],
              "organization": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "address": [
                      "string"
                    ],
                    "country": [
                      "string"
                    ],
                    "description": [
                      "string"
                    ],
                    "mainCountry": [
                      "string"
                    ],
                    "name": [
                      "Ava Chen"
                    ],
                    "permId": [
                      "string"
                    ],
                    "topics": [
                      "string"
                    ],
                    "website": [
                      "string"
                    ]
                  },
                  "referents": [
                    "string"
                  ],
                  "schema": "string",
                  "target": true
                }
              ],
              "role": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "middleName": [
          "Ava Chen"
        ],
        "modifiedAt": [
          "string"
        ],
        "name": [
          "Ava Chen"
        ],
        "nationality": [
          "string"
        ],
        "notes": [
          "string"
        ],
        "ownershipOwner": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "asset": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "buildDate": [
                      "string"
                    ],
                    "callSign": [
                      "string"
                    ],
                    "deadweightTonnage": [
                      "string"
                    ],
                    "description": [
                      "string"
                    ],
                    "flag": [
                      "string"
                    ],
                    "grossRegisteredTonnage": [
                      "string"
                    ],
                    "imoNumber": [
                      "string"
                    ],
                    "mmsi": [
                      "string"
                    ],
                    "name": [
                      "Ava Chen"
                    ],
                    "pastFlags": [
                      "string"
                    ],
                    "programId": [
                      "string"
                    ],
                    "sourceUrl": [
                      "https://example.com"
                    ],
                    "topics": [
                      "string"
                    ],
                    "type": [
                      "string"
                    ]
                  },
                  "referents": [
                    "string"
                  ],
                  "schema": "string",
                  "target": true
                }
              ],
              "owner": [
                "string"
              ],
              "role": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "political": [
          "string"
        ],
        "position": [
          "string"
        ],
        "positionOccupancies": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "holder": [
                "string"
              ],
              "post": [
                {
                  "caption": "string",
                  "datasets": [
                    "string"
                  ],
                  "firstSeen": "string",
                  "id": "string",
                  "lastChange": "string",
                  "lastSeen": "string",
                  "properties": {
                    "country": [
                      "string"
                    ],
                    "name": [
                      "Ava Chen"
                    ],
                    "topics": [
                      "string"
                    ]
                  },
                  "referents": [
                    "string"
                  ],
                  "schema": "string",
                  "target": true
                }
              ],
              "status": [
                "string"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "programId": [
          "string"
        ],
        "religion": [
          "string"
        ],
        "sanctions": [
          {
            "caption": "string",
            "datasets": [
              "string"
            ],
            "firstSeen": "string",
            "id": "string",
            "lastChange": "string",
            "lastSeen": "string",
            "properties": {
              "authority": [
                "string"
              ],
              "authorityId": [
                "string"
              ],
              "country": [
                "string"
              ],
              "entity": [
                "string"
              ],
              "listingDate": [
                "string"
              ],
              "program": [
                "string"
              ],
              "programId": [
                "string"
              ],
              "programUrl": [
                "https://example.com"
              ],
              "reason": [
                "string"
              ],
              "sourceUrl": [
                "https://example.com"
              ]
            },
            "schema": "string",
            "target": true
          }
        ],
        "sourceUrl": [
          "https://example.com"
        ],
        "taxNumber": [
          "string"
        ],
        "title": [
          "string"
        ],
        "topics": [
          "string"
        ],
        "uniqueEntityId": [
          "string"
        ],
        "unknownLinkFrom": [
          {
            "caption": "https://example.com",
            "datasets": [
              "https://example.com"
            ],
            "firstSeen": "https://example.com",
            "id": "https://example.com",
            "lastChange": "https://example.com",
            "lastSeen": "https://example.com",
            "properties": {
              "object": [
                "https://example.com"
              ],
              "role": [
                "https://example.com"
              ],
              "subject": [
                {
                  "caption": "https://example.com",
                  "datasets": [
                    "https://example.com"
                  ],
                  "firstSeen": "https://example.com",
                  "id": "https://example.com",
                  "lastChange": "https://example.com",
                  "lastSeen": "https://example.com",
                  "properties": {
                    "address": [
                      "https://example.com"
                    ],
                    "addressEntity": [
                      "https://example.com"
                    ],
                    "alias": [
                      "https://example.com"
                    ],
                    "birthCountry": [
                      "https://example.com"
                    ],
                    "birthDate": [
                      "https://example.com"
                    ],
                    "birthPlace": [
                      "https://example.com"
                    ],
                    "citizenship": [
                      "https://example.com"
                    ],
                    "country": [
                      "https://example.com"
                    ],
                    "createdAt": [
                      "https://example.com"
                    ],
                    "education": [
                      "https://example.com"
                    ],
                    "fatherName": [
                      "https://example.com"
                    ],
                    "firstName": [
                      "https://example.com"
                    ],
                    "gender": [
                      "https://example.com"
                    ],
                    "innCode": [
                      "https://example.com"
                    ],
                    "lastName": [
                      "https://example.com"
                    ],
                    "middleName": [
                      "https://example.com"
                    ],
                    "modifiedAt": [
                      "https://example.com"
                    ],
                    "name": [
                      "https://example.com"
                    ],
                    "nationality": [
                      "https://example.com"
                    ],
                    "notes": [
                      "https://example.com"
                    ],
                    "position": [
                      "https://example.com"
                    ],
                    "programId": [
                      "https://example.com"
                    ],
                    "sourceUrl": [
                      "https://example.com"
                    ],
                    "topics": [
                      "https://example.com"
                    ],
                    "uniqueEntityId": [
                      "https://example.com"
                    ],
                    "wikidataId": [
                      "https://example.com"
                    ],
                    "wikipediaUrl": [
                      "https://example.com"
                    ]
                  },
                  "referents": [
                    "https://example.com"
                  ],
                  "schema": "https://example.com",
                  "target": true
                }
              ]
            },
            "schema": "https://example.com",
            "target": true
          }
        ],
        "unknownLinkTo": [
          {
            "caption": "https://example.com",
            "datasets": [
              "https://example.com"
            ],
            "firstSeen": "https://example.com",
            "id": "https://example.com",
            "lastChange": "https://example.com",
            "lastSeen": "https://example.com",
            "properties": {
              "object": [
                {
                  "caption": "https://example.com",
                  "datasets": [
                    "https://example.com"
                  ],
                  "firstSeen": "https://example.com",
                  "id": "https://example.com",
                  "lastChange": "https://example.com",
                  "lastSeen": "https://example.com",
                  "properties": {
                    "country": [
                      "https://example.com"
                    ],
                    "name": [
                      "https://example.com"
                    ],
                    "registrationNumber": [
                      "https://example.com"
                    ],
                    "topics": [
                      "https://example.com"
                    ]
                  },
                  "schema": "https://example.com",
                  "target": true
                }
              ],
              "role": [
                "https://example.com"
              ],
              "subject": [
                "https://example.com"
              ]
            },
            "schema": "https://example.com",
            "target": true
          }
        ],
        "weakAlias": [
          "string"
        ],
        "website": [
          "string"
        ],
        "wikidataId": [
          "string"
        ],
        "wikipediaUrl": [
          "https://example.com"
        ]
      },
      "referents": [
        "string"
      ],
      "schema": "string",
      "target": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caption` | string |  |
| `datasets[]` | string |  |
| `firstSeen` | string |  |
| `id` | string |  |
| `lastChange` | string |  |
| `lastSeen` | string |  |
| `properties.address[]` | string |  |
| `properties.addressEntity[].caption` | string |  |
| `properties.addressEntity[].datasets[]` | string |  |
| `properties.addressEntity[].firstSeen` | string |  |
| `properties.addressEntity[].id` | string |  |
| `properties.addressEntity[].lastChange` | string |  |
| `properties.addressEntity[].lastSeen` | string |  |
| `properties.addressEntity[].properties.city[]` | string |  |
| `properties.addressEntity[].properties.country[]` | string |  |
| `properties.addressEntity[].properties.full[]` | string |  |
| `properties.addressEntity[].properties.street[]` | string |  |
| `properties.addressEntity[].schema` | string |  |
| `properties.addressEntity[].target` | boolean |  |
| `properties.alias[]` | string |  |
| `properties.associations[].caption` | string |  |
| `properties.associations[].datasets[]` | string |  |
| `properties.associations[].firstSeen` | string |  |
| `properties.associations[].id` | string |  |
| `properties.associations[].lastChange` | string |  |
| `properties.associations[].lastSeen` | string |  |
| `properties.associations[].properties.associate[]` | string |  |
| `properties.associations[].properties.person[].caption` | string |  |
| `properties.associations[].properties.person[].datasets[]` | string |  |
| `properties.associations[].properties.person[].firstSeen` | string |  |
| `properties.associations[].properties.person[].id` | string |  |
| `properties.associations[].properties.person[].lastChange` | string |  |
| `properties.associations[].properties.person[].lastSeen` | string |  |
| `properties.associations[].properties.person[].properties.address[]` | string |  |
| `properties.associations[].properties.person[].properties.addressEntity[]` | string |  |
| `properties.associations[].properties.person[].properties.alias[]` | string |  |
| `properties.associations[].properties.person[].properties.birthCountry[]` | string |  |
| `properties.associations[].properties.person[].properties.birthDate[]` | string |  |
| `properties.associations[].properties.person[].properties.birthPlace[]` | string |  |
| `properties.associations[].properties.person[].properties.citizenship[]` | string |  |
| `properties.associations[].properties.person[].properties.country[]` | string |  |
| `properties.associations[].properties.person[].properties.createdAt[]` | string |  |
| `properties.associations[].properties.person[].properties.education[]` | string |  |
| `properties.associations[].properties.person[].properties.fatherName[]` | string |  |
| `properties.associations[].properties.person[].properties.firstName[]` | string |  |
| `properties.associations[].properties.person[].properties.gender[]` | string |  |
| `properties.associations[].properties.person[].properties.innCode[]` | string |  |
| `properties.associations[].properties.person[].properties.lastName[]` | string |  |
| `properties.associations[].properties.person[].properties.middleName[]` | string |  |
| `properties.associations[].properties.person[].properties.modifiedAt[]` | string |  |
| `properties.associations[].properties.person[].properties.name[]` | string |  |
| `properties.associations[].properties.person[].properties.nationality[]` | string |  |
| `properties.associations[].properties.person[].properties.notes[]` | string |  |
| `properties.associations[].properties.person[].properties.position[]` | string |  |
| `properties.associations[].properties.person[].properties.programId[]` | string |  |
| `properties.associations[].properties.person[].properties.sourceUrl[]` | string |  |
| `properties.associations[].properties.person[].properties.topics[]` | string |  |
| `properties.associations[].properties.person[].properties.uniqueEntityId[]` | string |  |
| `properties.associations[].properties.person[].properties.wikidataId[]` | string |  |
| `properties.associations[].properties.person[].properties.wikipediaUrl[]` | string |  |
| `properties.associations[].properties.person[].referents[]` | string |  |
| `properties.associations[].properties.person[].schema` | string |  |
| `properties.associations[].properties.person[].target` | boolean |  |
| `properties.associations[].properties.relationship[]` | string |  |
| `properties.associations[].properties.sourceUrl[]` | string |  |
| `properties.associations[].schema` | string |  |
| `properties.associations[].target` | boolean |  |
| `properties.birthCountry[]` | string |  |
| `properties.birthDate[]` | string |  |
| `properties.birthPlace[]` | string |  |
| `properties.citizenship[]` | string |  |
| `properties.classification[]` | string |  |
| `properties.country[]` | string |  |
| `properties.createdAt[]` | string |  |
| `properties.description[]` | string |  |
| `properties.documentedBy[].caption` | string |  |
| `properties.documentedBy[].datasets[]` | string |  |
| `properties.documentedBy[].firstSeen` | string |  |
| `properties.documentedBy[].id` | string |  |
| `properties.documentedBy[].lastChange` | string |  |
| `properties.documentedBy[].lastSeen` | string |  |
| `properties.documentedBy[].properties.date[]` | string |  |
| `properties.documentedBy[].properties.document[].caption` | string |  |
| `properties.documentedBy[].properties.document[].datasets[]` | string |  |
| `properties.documentedBy[].properties.document[].firstSeen` | string |  |
| `properties.documentedBy[].properties.document[].id` | string |  |
| `properties.documentedBy[].properties.document[].lastChange` | string |  |
| `properties.documentedBy[].properties.document[].lastSeen` | string |  |
| `properties.documentedBy[].properties.document[].properties.publishedAt[]` | string |  |
| `properties.documentedBy[].properties.document[].properties.sourceUrl[]` | string |  |
| `properties.documentedBy[].properties.document[].properties.title[]` | string |  |
| `properties.documentedBy[].properties.document[].schema` | string |  |
| `properties.documentedBy[].properties.document[].target` | boolean |  |
| `properties.documentedBy[].properties.entity[]` | string |  |
| `properties.documentedBy[].schema` | string |  |
| `properties.documentedBy[].target` | boolean |  |
| `properties.education[]` | string |  |
| `properties.ethnicity[]` | string |  |
| `properties.familyPerson[].caption` | string |  |
| `properties.familyPerson[].datasets[]` | string |  |
| `properties.familyPerson[].firstSeen` | string |  |
| `properties.familyPerson[].id` | string |  |
| `properties.familyPerson[].lastChange` | string |  |
| `properties.familyPerson[].lastSeen` | string |  |
| `properties.familyPerson[].properties.person[]` | string |  |
| `properties.familyPerson[].properties.relationship[]` | string |  |
| `properties.familyPerson[].properties.relative[].caption` | string |  |
| `properties.familyPerson[].properties.relative[].datasets[]` | string |  |
| `properties.familyPerson[].properties.relative[].firstSeen` | string |  |
| `properties.familyPerson[].properties.relative[].id` | string |  |
| `properties.familyPerson[].properties.relative[].lastChange` | string |  |
| `properties.familyPerson[].properties.relative[].lastSeen` | string |  |
| `properties.familyPerson[].properties.relative[].properties.alias[]` | string |  |
| `properties.familyPerson[].properties.relative[].properties.birthDate[]` | string |  |
| `properties.familyPerson[].properties.relative[].properties.birthPlace[]` | string |  |
| `properties.familyPerson[].properties.relative[].properties.citizenship[]` | string |  |
| `properties.familyPerson[].properties.relative[].properties.firstName[]` | string |  |
| `properties.familyPerson[].properties.relative[].properties.gender[]` | string |  |
| `properties.familyPerson[].properties.relative[].properties.lastName[]` | string |  |
| `properties.familyPerson[].properties.relative[].properties.name[]` | string |  |
| `properties.familyPerson[].properties.relative[].properties.notes[]` | string |  |
| `properties.familyPerson[].properties.relative[].properties.topics[]` | string |  |
| `properties.familyPerson[].properties.relative[].properties.weakAlias[]` | string |  |
| `properties.familyPerson[].properties.relative[].properties.wikidataId[]` | string |  |
| `properties.familyPerson[].properties.relative[].properties.wikipediaUrl[]` | string |  |
| `properties.familyPerson[].properties.relative[].schema` | string |  |
| `properties.familyPerson[].properties.relative[].target` | boolean |  |
| `properties.familyPerson[].properties.sourceUrl[]` | string |  |
| `properties.familyPerson[].referents[]` | string |  |
| `properties.familyPerson[].schema` | string |  |
| `properties.familyPerson[].target` | boolean |  |
| `properties.familyRelative[].caption` | string |  |
| `properties.familyRelative[].datasets[]` | string |  |
| `properties.familyRelative[].firstSeen` | string |  |
| `properties.familyRelative[].id` | string |  |
| `properties.familyRelative[].lastChange` | string |  |
| `properties.familyRelative[].lastSeen` | string |  |
| `properties.familyRelative[].properties.person[].caption` | string |  |
| `properties.familyRelative[].properties.person[].datasets[]` | string |  |
| `properties.familyRelative[].properties.person[].firstSeen` | string |  |
| `properties.familyRelative[].properties.person[].id` | string |  |
| `properties.familyRelative[].properties.person[].lastChange` | string |  |
| `properties.familyRelative[].properties.person[].lastSeen` | string |  |
| `properties.familyRelative[].properties.person[].properties.address[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.alias[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.birthCountry[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.birthDate[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.birthPlace[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.citizenship[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.country[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.createdAt[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.education[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.fatherName[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.firstName[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.gender[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.idNumber[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.innCode[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.lastName[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.middleName[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.modifiedAt[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.name[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.nationality[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.notes[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.position[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.programId[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.sourceUrl[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.taxNumber[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.topics[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.uniqueEntityId[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.wikidataId[]` | string |  |
| `properties.familyRelative[].properties.person[].properties.wikipediaUrl[]` | string |  |
| `properties.familyRelative[].properties.person[].referents[]` | string |  |
| `properties.familyRelative[].properties.person[].schema` | string |  |
| `properties.familyRelative[].properties.person[].target` | boolean |  |
| `properties.familyRelative[].properties.relationship[]` | string |  |
| `properties.familyRelative[].properties.relative[]` | string |  |
| `properties.familyRelative[].schema` | string |  |
| `properties.familyRelative[].target` | boolean |  |
| `properties.fatherName[]` | string |  |
| `properties.firstName[]` | string |  |
| `properties.gender[]` | string |  |
| `properties.identification[].caption` | string |  |
| `properties.identification[].datasets[]` | string |  |
| `properties.identification[].firstSeen` | string |  |
| `properties.identification[].id` | string |  |
| `properties.identification[].lastChange` | string |  |
| `properties.identification[].lastSeen` | string |  |
| `properties.identification[].properties.holder[]` | string |  |
| `properties.identification[].schema` | string |  |
| `properties.identification[].target` | boolean |  |
| `properties.lastName[]` | string |  |
| `properties.membershipMember[].caption` | string |  |
| `properties.membershipMember[].datasets[]` | string |  |
| `properties.membershipMember[].firstSeen` | string |  |
| `properties.membershipMember[].id` | string |  |
| `properties.membershipMember[].lastChange` | string |  |
| `properties.membershipMember[].lastSeen` | string |  |
| `properties.membershipMember[].properties.member[]` | string |  |
| `properties.membershipMember[].properties.organization[].caption` | string |  |
| `properties.membershipMember[].properties.organization[].datasets[]` | string |  |
| `properties.membershipMember[].properties.organization[].firstSeen` | string |  |
| `properties.membershipMember[].properties.organization[].id` | string |  |
| `properties.membershipMember[].properties.organization[].lastChange` | string |  |
| `properties.membershipMember[].properties.organization[].lastSeen` | string |  |
| `properties.membershipMember[].properties.organization[].properties.address[]` | string |  |
| `properties.membershipMember[].properties.organization[].properties.country[]` | string |  |
| `properties.membershipMember[].properties.organization[].properties.description[]` | string |  |
| `properties.membershipMember[].properties.organization[].properties.mainCountry[]` | string |  |
| `properties.membershipMember[].properties.organization[].properties.name[]` | string |  |
| `properties.membershipMember[].properties.organization[].properties.permId[]` | string |  |
| `properties.membershipMember[].properties.organization[].properties.topics[]` | string |  |
| `properties.membershipMember[].properties.organization[].properties.website[]` | string |  |
| `properties.membershipMember[].properties.organization[].referents[]` | string |  |
| `properties.membershipMember[].properties.organization[].schema` | string |  |
| `properties.membershipMember[].properties.organization[].target` | boolean |  |
| `properties.membershipMember[].properties.role[]` | string |  |
| `properties.membershipMember[].schema` | string |  |
| `properties.membershipMember[].target` | boolean |  |
| `properties.middleName[]` | string |  |
| `properties.modifiedAt[]` | string |  |
| `properties.name[]` | string |  |
| `properties.nationality[]` | string |  |
| `properties.notes[]` | string |  |
| `properties.ownershipOwner[].caption` | string |  |
| `properties.ownershipOwner[].datasets[]` | string |  |
| `properties.ownershipOwner[].firstSeen` | string |  |
| `properties.ownershipOwner[].id` | string |  |
| `properties.ownershipOwner[].lastChange` | string |  |
| `properties.ownershipOwner[].lastSeen` | string |  |
| `properties.ownershipOwner[].properties.asset[].caption` | string |  |
| `properties.ownershipOwner[].properties.asset[].datasets[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].firstSeen` | string |  |
| `properties.ownershipOwner[].properties.asset[].id` | string |  |
| `properties.ownershipOwner[].properties.asset[].lastChange` | string |  |
| `properties.ownershipOwner[].properties.asset[].lastSeen` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.buildDate[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.callSign[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.deadweightTonnage[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.description[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.flag[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.grossRegisteredTonnage[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.imoNumber[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.mmsi[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.name[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.pastFlags[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.programId[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.sourceUrl[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.topics[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].properties.type[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].referents[]` | string |  |
| `properties.ownershipOwner[].properties.asset[].schema` | string |  |
| `properties.ownershipOwner[].properties.asset[].target` | boolean |  |
| `properties.ownershipOwner[].properties.owner[]` | string |  |
| `properties.ownershipOwner[].properties.role[]` | string |  |
| `properties.ownershipOwner[].schema` | string |  |
| `properties.ownershipOwner[].target` | boolean |  |
| `properties.political[]` | string |  |
| `properties.position[]` | string |  |
| `properties.positionOccupancies[].caption` | string |  |
| `properties.positionOccupancies[].datasets[]` | string |  |
| `properties.positionOccupancies[].firstSeen` | string |  |
| `properties.positionOccupancies[].id` | string |  |
| `properties.positionOccupancies[].lastChange` | string |  |
| `properties.positionOccupancies[].lastSeen` | string |  |
| `properties.positionOccupancies[].properties.holder[]` | string |  |
| `properties.positionOccupancies[].properties.post[].caption` | string |  |
| `properties.positionOccupancies[].properties.post[].datasets[]` | string |  |
| `properties.positionOccupancies[].properties.post[].firstSeen` | string |  |
| `properties.positionOccupancies[].properties.post[].id` | string |  |
| `properties.positionOccupancies[].properties.post[].lastChange` | string |  |
| `properties.positionOccupancies[].properties.post[].lastSeen` | string |  |
| `properties.positionOccupancies[].properties.post[].properties.country[]` | string |  |
| `properties.positionOccupancies[].properties.post[].properties.name[]` | string |  |
| `properties.positionOccupancies[].properties.post[].properties.topics[]` | string |  |
| `properties.positionOccupancies[].properties.post[].referents[]` | string |  |
| `properties.positionOccupancies[].properties.post[].schema` | string |  |
| `properties.positionOccupancies[].properties.post[].target` | boolean |  |
| `properties.positionOccupancies[].properties.status[]` | string |  |
| `properties.positionOccupancies[].schema` | string |  |
| `properties.positionOccupancies[].target` | boolean |  |
| `properties.programId[]` | string |  |
| `properties.religion[]` | string |  |
| `properties.sanctions[].caption` | string |  |
| `properties.sanctions[].datasets[]` | string |  |
| `properties.sanctions[].firstSeen` | string |  |
| `properties.sanctions[].id` | string |  |
| `properties.sanctions[].lastChange` | string |  |
| `properties.sanctions[].lastSeen` | string |  |
| `properties.sanctions[].properties.authority[]` | string |  |
| `properties.sanctions[].properties.authorityId[]` | string |  |
| `properties.sanctions[].properties.country[]` | string |  |
| `properties.sanctions[].properties.entity[]` | string |  |
| `properties.sanctions[].properties.listingDate[]` | string |  |
| `properties.sanctions[].properties.program[]` | string |  |
| `properties.sanctions[].properties.programId[]` | string |  |
| `properties.sanctions[].properties.programUrl[]` | string |  |
| `properties.sanctions[].properties.reason[]` | string |  |
| `properties.sanctions[].properties.sourceUrl[]` | string |  |
| `properties.sanctions[].schema` | string |  |
| `properties.sanctions[].target` | boolean |  |
| `properties.sourceUrl[]` | string |  |
| `properties.taxNumber[]` | string |  |
| `properties.title[]` | string |  |
| `properties.topics[]` | string |  |
| `properties.uniqueEntityId[]` | string |  |
| `properties.unknownLinkFrom[].caption` | string |  |
| `properties.unknownLinkFrom[].datasets[]` | string |  |
| `properties.unknownLinkFrom[].firstSeen` | string |  |
| `properties.unknownLinkFrom[].id` | string |  |
| `properties.unknownLinkFrom[].lastChange` | string |  |
| `properties.unknownLinkFrom[].lastSeen` | string |  |
| `properties.unknownLinkFrom[].properties.object[]` | string |  |
| `properties.unknownLinkFrom[].properties.role[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].caption` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].datasets[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].firstSeen` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].id` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].lastChange` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].lastSeen` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.address[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.addressEntity[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.alias[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.birthCountry[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.birthDate[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.birthPlace[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.citizenship[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.country[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.createdAt[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.education[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.fatherName[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.firstName[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.gender[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.innCode[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.lastName[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.middleName[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.modifiedAt[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.name[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.nationality[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.notes[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.position[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.programId[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.sourceUrl[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.topics[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.uniqueEntityId[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.wikidataId[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].properties.wikipediaUrl[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].referents[]` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].schema` | string |  |
| `properties.unknownLinkFrom[].properties.subject[].target` | boolean |  |
| `properties.unknownLinkFrom[].schema` | string |  |
| `properties.unknownLinkFrom[].target` | boolean |  |
| `properties.unknownLinkTo[].caption` | string |  |
| `properties.unknownLinkTo[].datasets[]` | string |  |
| `properties.unknownLinkTo[].firstSeen` | string |  |
| `properties.unknownLinkTo[].id` | string |  |
| `properties.unknownLinkTo[].lastChange` | string |  |
| `properties.unknownLinkTo[].lastSeen` | string |  |
| `properties.unknownLinkTo[].properties.object[].caption` | string |  |
| `properties.unknownLinkTo[].properties.object[].datasets[]` | string |  |
| `properties.unknownLinkTo[].properties.object[].firstSeen` | string |  |
| `properties.unknownLinkTo[].properties.object[].id` | string |  |
| `properties.unknownLinkTo[].properties.object[].lastChange` | string |  |
| `properties.unknownLinkTo[].properties.object[].lastSeen` | string |  |
| `properties.unknownLinkTo[].properties.object[].properties.country[]` | string |  |
| `properties.unknownLinkTo[].properties.object[].properties.name[]` | string |  |
| `properties.unknownLinkTo[].properties.object[].properties.registrationNumber[]` | string |  |
| `properties.unknownLinkTo[].properties.object[].properties.topics[]` | string |  |
| `properties.unknownLinkTo[].properties.object[].schema` | string |  |
| `properties.unknownLinkTo[].properties.object[].target` | boolean |  |
| `properties.unknownLinkTo[].properties.role[]` | string |  |
| `properties.unknownLinkTo[].properties.subject[]` | string |  |
| `properties.unknownLinkTo[].schema` | string |  |
| `properties.unknownLinkTo[].target` | boolean |  |
| `properties.weakAlias[]` | string |  |
| `properties.website[]` | string |  |
| `properties.wikidataId[]` | string |  |
| `properties.wikipediaUrl[]` | string |  |
| `referents[]` | string |  |
| `schema` | string |  |
| `target` | boolean |  |

## Native endpoint

Through the native OpenSanctions API, this operation is `GET /entities/:entity_id` (base URL `https://api.opensanctions.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-entity.md) for the provider-specific parameters and requirements.

