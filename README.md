# CryptoZombies_challenge

### zombiefactory.sol
    A contract is inherited from Ownable(has some methons to test owner, return owner, transfer 
	owner, etc). In this contract, we has a struct Zombie, and a Zombie struct has some properties 
	like name, dna, level, readyTime, winCount and lossCount. All zombies will push in a array, 
	zombies. Also has two mapping, zombieToOwner is using zombie's id to return who is the owner. 
	The other one uses address to mapping this address has how many zombies.
	#### 3 functions:
	1. _createZombie(string memory _name, uint _dna) internal, the index in the zombies is the id
	for the zombie. In this function, we will create a zombie, set the new zombie is owned by 
	msg.sender. Also, ownerZombieCount[msg.sender] ++;
	2. _generateRandomDna(string memory _str) private view returns (uint), izombie DNA should be
	16 digstes, so we do % in this function.
	3. createRandomZombie(string memory _name) public, if msg.sender doesn't has zombies, make a 
	rand DNA, and create a new zombie uses _createZombie with this DNA.
	