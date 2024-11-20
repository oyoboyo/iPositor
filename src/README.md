
# Vision

Positor aims to more closely couple the code assistant to the code:

- Assistant portability  
- Full contextual awareness
- Trust worthy editing and operation (e.g., file system, git)
- Low barrier to entry for non-coders

## Approach

- 
- Source controlled messages history (stored as threads(?))
- Docker 

# Table of contents

- Positor:
- Reactor: watches, and handles repository events, including messages
- Main: 
	- Repositories
	- 
	- Menu


# Mono Repo

This main mono repo is used for development of Positor apps and their dependancies.

The contents of this repository, is open source and open to contribution.

## Repository structure

```
packages/
  tools/ 
  models/
	  openai/
  positor/
apps/
  (iPositor)/
	  src/
		  main/
		  renderer
		  preload
```

- Packages: Contains shared packages e.g.:
	- Tools: i.e., tools available to the model
	- Models: i.e., connectors to various third party LLM services
	- Positor: 
		- a stateless, and asynchronous, context manager 
		- Takes a repository as argument
		- Processes for context
		- Returns a message array 
		- i.e., the positor, posits the current context
	- Reactor:
		- Watches the repository
		- Awaits events (i.e., file changes, new messages)
		- Orchestrates actions e.g.:
			- On user message:
				- Posit messages, 
				- Call model, 
				- write response message
			- On file change:
				- Posit messages
				- Call

Key question: what are the boundries of the Positor?

# Application Flow

### 

1. User Adds Repository
	1. From Files Dialog
	2. From Github

## Positor

1. Positor Receives Repository
2. Positor Processes Repository
	1. Processes Message
	2. Processes File Tree
	3. Processes Git History
	4. Processes Common Files e.g., package.json
3. Positor Summarizes Repository State & Recent History
5. Positor Returns Messages Stack Including Summary

##

