Storage is cheap, data isn't.


Datar

Gathers meta-data about a file, and allows for extra arbitrary data to be
associated with the file.  A the data is stored in a hidden, like-named
sibling of the file it refers to.  As well the data is stored in the application
data directory along with indexing data associated withe the file and its 
additional metadata.


APPLICATION DATA DIR
- index
-- index files
- metadata
-- file1.md


/<other location>
- file1 
- .file1.md

When Datar is installad on a system it makes friendly wrappers around common
operations such as mv, cp, and rm that will take into account any metadata
files for the files which are being operated on.

All of the data contained in the index is sourced from the metadata file and
the file itself.  The index is for lookups and can be recreated completely 
from the source material (you know, like an index).

