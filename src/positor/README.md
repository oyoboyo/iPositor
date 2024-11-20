# Positor API

- Receives a Repository path as argument, and a user prompt
- Builds a current state understanding of repository; incl. recent history of messages and events, repository contents, and meta data e.g., git diffs, current file system, readme files, package files, etc. 
- Returns a messages stack, with response
- Leveraged to 
	- Respond and act upon user input, and
	- React to repository events, e.g., commits, file system changes