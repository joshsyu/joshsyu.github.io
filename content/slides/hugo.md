+++
Categories = []
Tags = []
Title = "HUGO"
+++

# HUGO
---

	## Taxonomy
	 * User-defined grouping of content
	 * default: tags, categories

	## Definitions
	* Taxonomy: A categorization that can be used to classify content
	* Term: A key within that taxonomy
	* Value: A piece of content assigned to that Term
---
	## Example
	There are taxonomies:
	* Actor
	* Directors
	* Studios
	* Genre
	* ...
	Hugo would automatically create pages for each Actor, Director...  
	listing all of the Movie that matched specific Actor, Director
---
	## Example
	Actor                   <- Taxonomy
		Bruce Wills         <- Term
			The Siz Sense   <- Content
			Unbreakable     <- Content
		Samuel L. Jackson   <- Term
			Unbreakable     <- Content
			xXx             <- Content
---
	## Other display
	Unbreakable     			<- Content
		Actors 					<- Taxonomy
			Bruce Wills 		<- Term
			Samuel L. Jackson  	<- Term
		Director 				<- Taxonomy
			M. Night Shyamalan  <- Term
---
	## Usage
	1. Must be defined in the site configuration
		config.yaml:
		```
			taxonomies:
			tag: "tags"
			category: "categories"
			series: "series"
		```
	2. Assigning taxonomy values to content
		Front Matter Example:
		```
		title = "Movie"
		tags = ["Development", "Go"]
		categories = ["Development"]
		series = ["Go Web Dev"]
		```
---
## Display
	* Displaying taxonomy terms assigned to this content
	* Listing content with the same taxonomy term
	* Listing all content in a given taxonomy
	* Rendering a Site's taxonomies
	
