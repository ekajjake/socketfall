

# MVP Acceptance Criteria

Verbal description of requirements for MVP.

### Vocab

`Session` the WebSocket connection that should remain active as long as there are users

`Team` users are either on the Spy team or the Non-Spies

### 1. King (host)

The king needs to be able to create a game, receive a code for distribution to the rest of the players, and then be sent to a lobby.

1. King can visit splash page and click 'New Game' (0% / 0% / Josh)
2. King can enter a name for the game and click 'Create Game'
3. King gets sent to the lobby for the game where they can see a unique invite code

### 2. Plebeian (friend of host)

The rest of the host's friends need to be able to join an existing game given a code and then be sent to a lobby

1. Pleb can visit splash page, enter a code, and click 'Join Game'
2. If code is valid, Pleb gets sent to the lobby
3. If code is not valid, Pleb receives try again message

### 3. Everyone (Lobby)

1. Users can see who is in the lobby and this is updated asynchronously
2. Any user can start or leave the session at any point
  1. Starting a game
    1. Triggers a game started event for all other users in the lobby async
    2. All users are sent to the Game view
  2. Leaving a game
    1. Sends the user to the home screen
    2. Ends the session

### 4. Everyone (Game)

1. A spy is selected among the users
2. Non-spies receive a location
3. All users can list of potential locations
4. There is a countdown timer that sends everyone to the voting screen
5. Any user can end the game via 'End Game' button

# Non-MVP Acceptance Criteria

### 5. Everyone (Voting)

1. Can select one user to pick as the Spy
2. See the total number of votes for each user (updated async)
3. Can end the game

...
