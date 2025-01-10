git submodule add https://github.com/google/leveldb.git thirdparty/leveldb
git add .gitmodules thirdparty/leveldb
git commit -m "Add LevelDB as a submodule"
git push
================================================
cd thirdparty/leveldb
# Make changes and commit them
git add .
git commit -m "Custom modifications to LevelDB"

cd ../../
# Stage and commit the submodule pointer update in your main repo
git add thirdparty/leveldb
git commit -m "Update submodule pointer for custom LevelDB changes"
git push
