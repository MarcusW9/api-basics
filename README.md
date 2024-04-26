nDxeTUOdMw3YdgcdKrSrL48AMq4ifT8V

Main Takeaway / Issues:
Had an issue whilst making this whereby on line 28 for the "fallback" where I set a default gif. I initially
hardcoded this in so that it would return img.src = "hardcoded url". This worked but kept throwing an error in the console
it turned out that the next .then was still being triggered and being handed this line. 
The .then was expecting a promise to be handed which it could then find the data.data.images.original.url
So I needed to "package" the harcoded url instead into a "promise" with promise.resolve and the correct "structure" of data