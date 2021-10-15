# public-api-python

Public API for Public APIs
Build Status Go Report Card

Welcome to the official public API for the public-apis project!

This service supports CORS and requires no authentication to use. All responses are sent over HTTPS as well.

Base URL
https://api.publicapis.org/

Services
GET /entries
List all entries currently cataloged in the project

Parameters
Parameter	Type	Data Type	Description	Required
title	query	string	name of entry (matches via substring - i.e. "at" would return "cat" and "atlas")	No
description	query	string	description of entry (matches via substring)	No
auth	query	string	auth type of entry (can only be values matching in project or null)	No
https	query	bool	return entries that support HTTPS or not	No
cors	query	string	CORS support for entry ("yes", "no", or "unknown")	No
category	query	string	return entries of a specific category	No
For categories like "Science & Math" which have a space and an ampersand, the query is simply the first word. Using "Science & Math" as an example, the correct query would be category=science

GET /random
List a single entry selected at random

Parameters
Parameter	Type	Data Type	Description	Required
title	query	string	name of entry (matches via substring - i.e. "at" would return "cat" and "atlas")	No
description	query	string	description of entry (matches via substring)	No
auth	query	string	auth type of entry (can only be values matching in project or null)	No
https	query	bool	return entries that support HTTPS or not	No
cors	query	string	CORS support for entry ("yes", "no", or "unknown")	No
category	query	string	return entries of a specific category	No
GET /categories
List all categories

Parameters
None

GET /health
Check health of the running service

Parameters
None
