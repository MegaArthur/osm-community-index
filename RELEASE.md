## Release Checklist

### Icons
This project bundles some icons from FontAwesome, corresponding to the types of
community resources.  Whenever the list of resource types changes:
- [ ] Edit `build_icons.js`
- [ ] npm run icons

### Update master branch
- [ ] git checkout master
- [ ] npm install
- [ ] npm run test
- [ ] npm run txpull
- [ ] git add . && git commit -m 'npm run txpull'
- [ ] Update `CHANGELOG.md`
- [ ] Update version number in `package.json`
- [ ] git add . && git commit -m 'vA.B.C'
- [ ] git push origin master

### Update release branch, tag and publish
- [ ] git checkout release
- [ ] git reset --hard master
- [ ] npm run build
- [ ] npm run dist
- [ ] git add -f dist/*
- [ ] git commit -m 'Check in build'
- [ ] git tag vA.B.C
- [ ] git push origin -f release vA.B.C
- [ ] npm publish

Open https://github.com/osmlab/osm-community-index/tags
Click "Add Release Notes" and link to the CHANGELOG
