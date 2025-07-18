# 🤖 Commands

## Table of contents

- [Inside a Modmail thread](#inside-a-modmail-thread)
- [Anywhere on the inbox server](#anywhere-on-the-inbox-server)
- [Snippets (canned messages)](#snippets-canned-messages)

## Inside a Modmail thread

These commands can only be used inside a Modmail thread's channel on the inbox server.

### `=reply <text>` / `=r <text>`

Send a reply to the user.

**Example:** `=r How can I help you?`

To reply automatically without using `=reply`, [turn on `alwaysReply` in bot settings](configuration.md).

### `=anonreply <text>` / `=ar <text>`

Send an anonymous reply to the user. Anonymous replies only show the moderator's role in the reply.

**Example:** `=ar Please only use Modmail for serious messages`

To reply automatically without using `=reply`, [turn on `alwaysReply` in bot settings](configuration.md).

### `=realreply <text>` / `=rr <text>`

Send a reply to the user. This will always include the moderator's name, even if the `forceAnon` option is enabled.

### `=close`

Close the Modmail thread.

### `=close <time>`

Close the Modmail thread after a timer. Sending a message to the user or receiving a message from the user will cancel scheduled closing.

**Example:** `=close 15m`

### `=close -s` / `=close -s <time>`

Close the Modmail thread without notifying the user that it was closed.

### `=close cancel`

Cancel a timed close.

### `=logs`

List previous Modmail logs with the user.

### `=block`

Block the user from using Modmail.

### `=block <time>`

Block the user from using Modmail for a specified time.

**Example:** `=block 7d`

### `=unblock`

Unblock the user, allowing them to use Modmail again.

### `=move <category>`

Move the Modmail thread to a different category.
Requires `allowMove` to be enabled in the bot's settings.

### `=suspend`

Suspend the thread.
The thread will act as closed and will not receive any messages until unsuspended via `=unsuspend`.

### `=unsuspend`

Unsuspend the thread. See `=suspend` above.

### `=alert`

Pings you when the thread gets a new reply.

### `=alert cancel`

Cancel the ping set by `=alert`.

### `=edit <number> <new text>`

Edit your own previous reply sent with `=reply`.  
`<number>` is the message number shown in front of staff replies in the thread channel.

### `=delete <number>`

Delete your own previous reply sent with `=reply`.  
`<number>` is the message number shown in front of staff replies in the thread channel.

### `=role`

View your display role for the thread - the role that is shown in front of your name in your replies

### `=role reset`

Reset your display role for the thread to the default

### `=role <role name>`

Change your display role for the thread to any role you currently have

### `=loglink`

Get a link to the open Modmail thread's log.

### `=loglink -s`

Get a link to the open Modmail thread's log, only showing messages to/from the user (ignores mod chatter within the thread).

### `=loglink -v`

Get a link to the open Modmail thread's log, showing extra details about channel and message IDs between the bot and the user.
This is mainly useful when reporting messages to Discord's Trust & Safety team.

### `=id`

Prints the user's ID.

### `=note <text>`

Add a note for the user

### `=notes <userID>`

Show all notes for the user

### `=delete_note <noteID>`

Delete the specified note. The note ID is shown when running `=notes`.

### `=dm_channel_id`

Prints the ID of the current DM channel with the user

### `=message <number>`

Shows the DM channel ID, DM message ID, and message link of the specified user reply.
`<number>` is the message number shown in front of staff replies in the thread channel.

## Anywhere on the inbox server

These commands can be used anywhere on the inbox server, even outside Modmail threads.

### `=newthread <userID>`

Open a Modmail thread with a user.

**Example:** `=newthread 106391128718245888`

### `=logs <userID>`

List previous Modmail logs with the specified user.

**Example:** `=logs 106391128718245888`

### `=block <userID>`

Block the specified user from Modmail.

**Example:** `=block 106391128718245888`

### `=block <userID> <time>`

Block the specified user from Modmail for a specified time.

**Example:** `=block 106391128718245888 7d`

### `=unblock <userID>`

Unblock the specified user, allowing them to use Modmail again.

**Example:** `=unblock 106391128718245888`

### `=is_blocked <userID>`

Check if the specified user is blocked.

**Example:** `=is_blocked 106391128718245888`

### `=role`

(Outside a modmail thread) View your default display role - the role that is shown in front of your name in your replies

### `=role reset`

(Outside a modmail thread) Reset your default display role

### `=role <role name>`

(Outside a modmail thread) Change your default display role to any role you currently have

### `=note <userID> <text>`

Add a note for the specified user

### `=notes <userID>`

Show all notes for the specified user

### `=delete_note <noteID>`

Delete the specified note. The note ID is shown when running `=notes`.

### `=version`

Show the Modmail bot's version.

## Plugin Commands

### `=help`

Links to the documentation in Dragory's Repository

### `=ping`

Tests latency

### `=messageclose`

Use in a thread to close with just a message

### `=reasonclose`

Use in a thread to close with just a reason

### `=logsearch`

Allows everyone with permission to use the MM bot to search through the logs of a specified user or all logs ever created. If the command is run in a thread, the user it is with will always be taken as the search target.

#### Usage

Any system messages and commands are not taken into account when searching and are ignored.  
`userId` needs to be the users proper ID, obtainable in [developer mode](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-).

##### In A Thread

Signature: `=logsearch <search query>`  
This will return a list of all logs that contain what you searched for.  
The search will be executed for the current threads user.

##### In The Inbox Server

Signature: `=logsearch <userId> <search query>`  
This will return a list of all logs that contain what you searched for.  
The search will be executed for the userId you pass to the command.

Signature: `=logsearch global <search query>`  
This will return a list of all logs that contain what you searched for.  
The search will be executed globally, checking every log ever created.

## Snippets (canned messages)

See the [📋 Snippets](snippets.md) page for more information!
