# Charge
This endpoint charges a certain payment method a certain amount.

## This endpoint is untested, things may be documented incorrectly.

## Request
`POST` [/v1/charge](https://pay01.tsinfra.net/v1/charge)

### Example
Stripe:
```json
{
  "charge_type": "STRIPE", // Payment type
  "token": "tok_HGJKFDGYFTG768FUDIG", // https://stripe.com/docs/api/tokens/create_card
  "amount_stripe": 20, // Amount to charge
  "amount": 20, // Display amount (maybe?)
  "email": "example@teamseas.org", // Billing email
  "donation_id": "RANDOMDONATIONID", // Randomly generated donation id, can be anything, as long as it is unique.
  "name": "SLLCoding", // Billing name
  "display_name": "SLLCoding", // Display name
  "team_name": "SLLCoding", // Team name of person
  "message_public": "Hello World!", // Message to display with the donation
  "flair": "https://assets01.teamassets.net/assets/badges/feed-icon-1.png", // Flair of your choice
  "created_at": 0 // Epoch time of donation creation
}
```


## Response

### Example
Failure:
```json
{
  "success": false,
  "message": "ERROR_CREATING_CUSTOMER",
  "display_name": "SLLCoding",
  "email": "example@teamseas.org",
  "team_name": "SLLCoding",
  "flair": "feed-icon-1.png",
  "created_at": 1635700362
}
