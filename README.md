# CSSystems-HW3
Weihang Qin
Liam Goodwin

We included 
1. a basic test that tests for set(), get() and reset()
2. a deletion test 
3. an overwrite test for modifying the key
4. a null-evictor test for the behaviors of cache with memory capacity reached when passed in a nullptr
5. a deep copy test that tests if the set value is passed in as a deep copy
6. a collision test that deliberately maps two keys into the same slot. 
7. a fifo-test for fifo_evictor behavior in general

## Our Project tested
| Test name         | Result                  | Comment |
|-------------------|-------------------------|---------|
| basic test        | passed                  |         |
| deletion test     | passed                  |         |
| basic test        | passed                  |         |                                                                    
| deletion test     | passed                  |         |
| null-evictor test | passed                  |         |
| deep copy test    | passed                  |         |
| collision test    | passed                  |         |
| fifo evictor test | passed                  |         |

## First Project tested
| Test name         | Result                  | Comment                                                                    |
|-------------------|-------------------------|----------------------------------------------------------------------------|
| basic test        | failed                  | get() was not using the size parameter at all. reset throws an exception.  |
| deletion test     | failed                  | deleting the same element twice failed to return false                     |
| overwrite test    | passed except for reset |                                                                            |
| null-evictor test | passed except for reset |                                                                            |
| deep copy test    | passed except for reset |                                                                            |
| collision test    | passed except for reset |                                                                            |
| fifo evictor test | failed                  |                                                                            |


## Second Project tested
| Test name         | Result      | Comment                                                                       |
|-------------------|-------------|-------------------------------------------------------------------------------|
| basic test        | failed      | get() was calling evictor's touch_key method even if a nullptr was passed in. |
| deletion test     | cannot test | since get failed, we cannot test by asserting anymore                         |
| overwrite test    | cannot test | since get failed, we cannot test by asserting anymore                         |
| null-evictor test | cannot test | since get failed, we cannot test by asserting anymore                         |
| deep copy test    | cannot test | since get failed, we cannot test by asserting anymore                         |
| collision test    | cannot test | since get failed, we cannot test by asserting anymore                         |
| fifo evictor test | cannot test | since get failed, we cannot test by asserting anymore                         |



## Third Project tested
| Test name         | Result      | Comment                                                                                                                         |
|-------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------|
| basic test        | failed      | If a nullptr was passed in as evictor, the implementation intentionally crashed. size parameter in the get function is not used |
| deletion test     | failed      | exception thrown when deleting a variable called valcopy                                                                        |
| overwrite test    | failed      | exception thrown when deleting a variable called valcopy                                                                        |
| null-evictor test | cannot test | cannot pass nullptr in                                                                                                          |
| deep copy test    | passed      |                                                                                                                                 |
| collision test    | failed      | exception thrown when deleting a variable called valcopy                                                                        |
| fifo evictor test | failed      | exception thrown when deleting a variable called valcopy                                                                        |