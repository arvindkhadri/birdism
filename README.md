# Birdism

Portal for helping bird identification and much more. This application helps in narrowing down
identification of a bird. 

Often is the case when you have identified the family of the bird, but is unable to conclusively
identify the exact species. In that case, you frantically search for different species of that
family and looking at their photographs.

This application simply does it for you!

Enter a family name (flycatcher, eagle, ducks) and the region name - and this
application will list all the species of that family available in that region,
with multiple photographs. Helping you to identify your bird.

# How it works
This application uses the taxonomy database from ebird, and its checklist API to
find out all the species (of a family) in a particular region from last 30 days
of observation. Then it takes those common species name, and does a Flickr
search for photos, and displays them to you!

# Development
The backend is in Haskell (code resides in the `server` directory).

The frontend is planned in HyperApp. Right now its implemented in mithril.js (code resides in the `app` directory).

# License
BSD3 license. See LICENSE file.

# Contributing
Submit an issue or a pull request.

# To deploy
- Run `make image` to build the actual image. Then run `make push` to publish it.
- See if you're heroku CLI and all is setup properly
- Update `Dockerfile.heroku` to adjust the version accordingly
- Commit and run `git push heroku master`
