# Recent Donations
This endpoint shows the 120 most recent donations, the 120 top donations, all registered teams and the 20 top donating teams.

## Endpoint
`GET` [/json/lb_recent.json](https://assets01.teamassets.net/json/lb_recent.json)

## Example
```json
{
  "recent": [ // Top 120 most recent donations
    {
      "ff": 0, // Unknown value
      "name": "SLL", // Name of the person who donated
      "team_name": "SLLCoding", // Name of the team the person donated for, can be ""
      "message_public": "Hello World!", // Message that the person specified with their donation, can be ""
      "flair": "feed-icon-1.png", // The donation's flair image, can be found at endpoint: /images/<flair>
      "pounds": "10", // Amount of money donated, can contain commas
      "pounds_color": "FFB72B", // Hex colour associated with the donation
      "created_at": 1635694724 // Epoch time of donation creation
    }
  ],
  "teams": [ // All registered teams
    {
      "id": "SLLCoding", // Unique ID of the team
      "text": "SLLCoding" // Display name of the team
    }
  ],
  "most": [ // Top 120 biggest donations
    {
      "ff": 0,
      "name": "The Bikoff Foundation",
      "team_name": "",
      "message_public": "",
      "flair": "feed-icon-6.png",
      "pounds": "1,000,000",
      "pounds_color": "FFB72B",
      "created_at": 1635646053
    }
  ],
  "config": {}, // Unknown value
  "teams_alpha": [ // List of 20 teams, unknown order
     "team": "", // No team
     "total_donation": "3,845,603", // Total donated amount, can contain commas
     "total_members": "85763", // Total team members
     "sort_donation": "3845603" // Total donated amount, cannot contain commas
  ],
  "teams_most_donations": [ // Top 20 biggest donating teams
    "team": "YT_Total",
    "total_donation": "1,252,069",
    "total_members": "4",
    "sort_donation": "1252069"
  ]
}
```
