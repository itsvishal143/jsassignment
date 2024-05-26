/*
Assessment Requirements
1. Create a variable that can hold a number of NFT's. What type of variable might this be?
2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
   The metadata values will be passed to the function as parameters. When the NFT is ready, 
   you will store it in the variable you created in step 1
3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
4. For good measure, getTotalSupply() should return the number of NFT's you have created
*/

// create a variable to hold your NFT's

let nftCollection = [];

// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT(name, description, image) {
  // Create an object to hold the metadata for the NFT
  let nft = {
    name: name,
    description: description,
    image: image
  };
  
  // Add the NFT to the collection
  nftCollection.push(nft);
}

// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
// Function to list all NFTs in the collection
function listNFTs() {
  for (let i = 0; i < nftCollection.length; i++) {
    let nft = nftCollection[i];
    console.log("Name: " + nft.name);
    console.log("Description: " + nft.description);
    console.log("Image: " + nft.image);
    console.log("---------");
  }
}

// print the total number of NFTs we have minted to the console
function getTotalSupply() {
  return nftCollection.length;
}

// call your functions below this line
// Mint some NFTs
mintNFT("NFT 1", "This is the first NFT", "image1.png");
mintNFT("NFT 2", "This is the second NFT", "image2.png");
mintNFT("NFT 3", "This is the third NFT", "image3.png");

// List all NFTs in the collection
listNFTs();

// Get the total supply of NFTs in the collection
console.log("Total Supply: " + getTotalSupply());



