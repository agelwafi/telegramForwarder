# Database

### 1. User

- name (string)
- chat_id (string)
- username (string)
- ref_code (string)
- premium (Boolean)

### 2. Redirections

- owner
- source
- destination

# Features

## Free

1. /add -- Adding redirections allows you to setup a automatic routing of messages from any telegram channels to your own telegram channels
2. /activate -- Activate a redirection from your list. *Bot does automatic forwarding of messages only for active redirections*
3. /deactivate -- deactivates a redirection from your list.  Bot does not do automatic forwarding of messages for inactive re-directions
4. /list -- get list of redirections with their corresponding redirection IDs
5. /remove -- remove the redirection with id REDIRECTION_ID from your redirections list
6. /filters -- get information about filters, applied to redirection with id REDIRECTION_ID
7. /filter -- use filters allow you to make the bot skip messages that you do not want to be forwarded.
  Message can also be forwarded, but filter removes photos, documents, animations, stickers, links, hashtags, etc.
  Please see MultiFeed Bot for all filters it has that I want.  
    - FILTER_NAME = name of the filter 
    - REDIRECTION_ID = ID of the redirection for which you update the filter’s state
    - STATE = state of filter; use on for enabling filter and off for disabling it.
8. /me – gets information about your account (including information about activated paid bot features & invited users).
  List all PAID features with subscription end date.
  PAID features may have a different subscription end date, depending on date customer purchased it.
  Admin has the ability to enable/disable PAID features & change subscription end date for each feature.
9. /ref – Share referral link with others and get bonus. 
  +30 day subscription to all PAID features when referral pays for subscription.
  Assign unique referral link/ID for each subscriber.
  Admin will know which existing customer had referred the new subscriber.
  Admin will manually update subscription of subscriber’s account.

## Premium

1. Use copy-paste mode of forwarding 
  *Purpose*: Remove "Forwarded from" header (aka "link to the sourcing channel") from redirected messages
2. Connect Telegram account to Bot
  *Purpose*: Setup redirections from channels you don't have an invitation link for, but are a member of, which is the per-requisite for setting up redirections from/to bots, groups, people and transformation feature.
3. Enable Transformation
  *Purpose*: Replace particular words in messages with your own words.  Remove particular words or phrases in messages
4. Setup redirections from/to bots, groups, or people each direction 
5. The FREE version only offers up to 10 active redirections on your list.
  I would like the ability for PAID subscribers to buy package of 50 additional redirections.
  Admin has the ability to specify any # of redirections.
  Limit up to 100,000 redirections.
  No limit – unlimited would be great to have as well.
  *Purpose*: You want to have more than 10 active redirection on your list.  
    The number of messages, passing through your redirections, is unlimited anyways (for both free and paid redirections).
    So a single source (Channel) -> Bot counts as 1 redirection.  Or Bot -> Bot is another re-direction.


# WORKFLOW
1. Setup redirections from Bot, Channel (not an Admin), user -->  Bot, Channel or user.
  Will need to Connect Telegram account to Bot for this to work from what I’ve gathered in my Research.
  Connect to telegram account to Bot also required to enable transformation & copy-paste forwarding feature.
2. Enable transformation to replace a particular word from message (e.g. Tier: Gold -> Plan: Platinum)
3. Enable copy-paste of Forwarding to remove "Forwarded from" header (aka "link to the sourcing channel") from redirected messages – hiding source
4. Apply Filter to remove images, links, hashtags or certain keywords
5. Apply Filter to forward a message containing a specific keyword/phrase to specific Bot, Channel or user– redirection.  
  * Example#1: if message contains the keyword/phrase: “Plan: Platinum” -> Channel #1, Bot#1 or user#1.
  * Example#2: if message contains the keyword/phrase: “Plan: Gold” -> Channel#2, Bot#2 or user#2.
  * Example#3: if message contains the keyword/phrase: “Plan: Silver” -> Channel#3, Bot#3 or user#3.