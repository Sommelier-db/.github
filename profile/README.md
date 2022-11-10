# Sommelier DB
**Open source DB with public-key searchable encryption: discerning encrypted data without knowing the contents, just like a sommelier!**
![sommelier-db-logo](https://user-images.githubusercontent.com/31360991/201113252-98666c26-cc93-4a7e-98fb-67ea4e10a638.png)

## What is Sommelier DB?
Sommelier DB is **an open source DB library combining SQLite and public-key searchable encryption (PKSE)**. In addition to existing SQLite features, it provides functions for PKSE as below.

1. A new SQL function to test a keyword encryption of the PKSE scheme.
2. C and Rust functions to generate a keyword encryption and a trapdoor of the PKSE scheme.

## What is Sommelier Drive?
Sommelier Drive is a remote file system developed as the first application of Sommelier DB. Its stored files and their file paths are encrypted with the public key of the legitimate user who has read permission to the file. Therefore, **other users who do not have the read permission or the administrator of the server hosting the file system cannot know what files exist and where they are located**. Furthermore, the legitimate users can generate trapdoors using the user's private key, allowing the server to search for the appropriate file without revealing the search criteria.

![Demo](https://user-images.githubusercontent.com/51953536/201111228-d08b5477-8808-41d6-9f05-5bd4487f9ab1.gif)

For more information, see [our document page](https://sommelier-db.github.io/Sommelier-docs/)!