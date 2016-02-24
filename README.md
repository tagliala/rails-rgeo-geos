# Test rgeo on heroku

1. Create app `heroku create`
2. Set environment variables `heroku config:set BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi.git LD_LIBRARY_PATH=/app/lib`
3. Push to heroku
4. Switch to a specific rgeo branch (eg: rgeo-0.5.3, rgeo-0.5.2)
5. Push force to heroku (eg: `git push -f rgeo-0.5.3 heroku:master`)
6. Run `heroku run console`
7. Check if GEOS is supported via `RGeo::Geos.supported?`
8. Repeat from point 4 specifying a different branch
