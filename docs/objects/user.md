---
slug: /objects/user
sidebar_label: User
---

# User

### Structure
| Field | Type | Description | Optional | Deprecated |
| - | - | - | - | - |
| _id | string | The user's username. |
| lower_username | string | The lower-case version of the user's username. |
| uuid | UUID4 | The user's UUID4. |
| created | integer | The user's creation timestamp in Unix seconds. |
| pfp_data | integer | The user's selected profile picture. |
| quote | string | The user's quote. |
| flags | integer | The user's flags. |
| permissions | integer | The user's admin permissions. |
| lvl | integer | The user's admin level. | | ✓ |
| ban* | [User Ban object](/objects/user-ban) | Ban status associated with the user. | ✓ | |
| banned | boolean | Whether the user is currently banned. |
| last_seen | integer | The timestamp in Unix seconds of when the user was last online. |
| delete_after* | integer | The timestamp in Unix seconds of when the user is scheduled to be deleted. | ✓ | |

**\* These fields are only returned when a user is fetching their own user profile.**

### Examples
#### Own user profile
```json
{
    "_id": "MikeDEV",
    "lower_username": "mikedev",
    "uuid": "a887becf-fe1d-492a-92c3-e2af7d15db28",
    "created": 1649983115,
    "pfp_data": 26,
    "quote": "🦆👋 Friendly neighborhood duck enthusiast. Owner of Meower!",
    "flags": 0,
    "permissions": 1,
    "lvl": 0,
    "ban": {
        "state": "none",
        "restrictions": 0,
        "expires": 0,
        "reason": ""
    },
    "banned": false,
    "last_seen": 1706574821,
    "delete_after": null
}
```

#### Other user profile
```json
{
    "_id": "MikeDEV",
    "lower_username": "mikedev",
    "uuid": "a887becf-fe1d-492a-92c3-e2af7d15db28",
    "created": 1649983115,
    "pfp_data": 26,
    "quote": "🦆👋 Friendly neighborhood duck enthusiast. Owner of Meower!",
    "flags": 0,
    "permissions": 1,
    "lvl": 0,
    "banned": false,
    "last_seen": 1706574821
}
```
