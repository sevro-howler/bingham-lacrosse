# GroupMe Groups

All GroupMe groups for Bingham Youth Lacrosse communication.

---

## Parent Groups

### Bingham 2/3 Spring 2026
- **Type:** Parent Communication
- **Group ID:** 113163957
- **Teams:** 2/3
- **Members:** All 2/3 parents
- **Purpose:** Game updates, schedule changes, snack signup

### Bingham 3/4 Spring 2026 (Combined)
- **Type:** Parent Communication
- **Group ID:** 113163960
- **Teams:** 3/4 Blue + 3/4 White
- **Members:** All 3/4 parents
- **Purpose:** General 3/4 communication (may split into separate groups)

### Bingham 3/4 White Spring 2026
- **Type:** Parent Communication
- **Group ID:** 113813364
- **Teams:** 3/4 White only
- **Join Link:** https://groupme.com/join_group/113813364/MPenhVre
- **Members:** 19 (White team parents)
- **Created:** March 14, 2026
- **Purpose:** White team-specific communication

---

## Coach Groups

### Bingham 2/3 Coaches Spring 2026
- **Type:** Coach Communication
- **Group ID:** 113164088
- **Purpose:** Coach coordination for 2/3 team

### Bingham 3/4 Coaches Spring 2026
- **Type:** Coach Communication
- **Group ID:** 113164089
- **Purpose:** Coach coordination for 3/4 teams

---

## API Reference

### GroupMe API Endpoints

**Base URL:** `https://api.groupme.com/v3`

**Authentication:** Token passed as query parameter

**Common Operations:**

```bash
# List all groups
GET /groups?token=$GROUPME_TOKEN&per_page=50

# Get specific group
GET /groups/{group_id}?token=$GROUPME_TOKEN

# Send message to group
POST /groups/{group_id}/messages?token=$GROUPME_TOKEN
Content-Type: application/json
{
  "message": {
    "source_guid": "unique-id",
    "text": "Message text"
  }
}

# Add members to group
POST /groups/{group_id}/members/add?token=$GROUPME_TOKEN
Content-Type: application/json
{
  "members": [
    {"phone_number": "+1XXXXXXXXXX", "nickname": "Name"}
  ]
}

# Create new group
POST /groups?token=$GROUPME_TOKEN
Content-Type: application/json
{
  "name": "Group Name",
  "share": true
}
```

---

## Group Management Notes

### Parent Group Strategy
- **2/3:** Single group (smaller team)
- **3/4:** Split into Blue and White groups as needed
  - White group already created (113813364)
  - Blue group may need creation if separate communication needed

### Adding Parents to Groups
When adding parents:
1. Use phone numbers from parent-contacts.md
2. Include both parents where applicable
3. Use format: `"First Last (Player parent)"`
4. Verify phone numbers are current

### Message Templates
See [parent-messages.md](./parent-messages.md) for templates.

---

*Last updated: March 17, 2026*
