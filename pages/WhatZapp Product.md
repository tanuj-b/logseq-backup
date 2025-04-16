- Jobs to be Done
	- Separation between life and work
	- Automating "etiquettes" & "people-skills"
		- Birthdays reminder
		- Thank you message after a meeting
		- Personalised greeting to Updates from Social media
	- Auto populating "follow-ups", "scheduled meetings" & "todo"
- Flows for v1
  id:: 67d009ce-6338-404e-a9db-7ffd11ff5f06
	- Message Summary based flow
		- Take the summary of last messages since the cursor
		- Read every conversation and for each, derive:
			- One line and one paragraph summary
			- Action Items for self
			- Follow-up with the other person
			- Ideal response in flavours (yes/no/etc.)
			- If it matches User-written filter
				- Apply User-defined Tag so that appears in list
		- After doing the above for all conversations:
			- Create a Mega Summary from all the one line summaries
			  logseq.order-list-type:: number
				- include tags, give priority to user filters, etc.
				  logseq.order-list-type:: number
			- Enter Blaze mode
			  logseq.order-list-type:: number
				- show one message and auto responses, let them choose. If they want to respond manually, add tag "open threads" and move on. Once clicked on an option, move to next.
				  logseq.order-list-type:: number
				- After they finish, ask them to deal with open threads list on whatsapp.
				  logseq.order-list-type:: number
- Data Structures and state management for ((67d009ce-6338-404e-a9db-7ffd11ff5f06))
	- We must retain a copy of every message in the DB.
		- Given that history is not yet cracked, we only have the possibility of saving every message when we get it. We use this local saved db of messages as our source of truth.
	- "STATE" -> Unique to the user
		- Message DB
		- Pointer  to last checkpoint (timestamp)
		- User Rules / Preferences
		- Lists we create
			- Action Items
			- Followups
		- Log of Actions from users
- The future of this product - [[Vision for Bitfool]]
-