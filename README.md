# JSTest(NFT.js)
This Java script program NFT.js, in this I have created and listed NFTs.


## Description

This program is a simple mininting NFTs written in Java script. In this java script program created NFT object by passing the metadata as function parameters/arguements  and listed the minted NFs by iterating the array NFTs and finally get the total supply of the minted NFTs


## Getting Started


### Executing program

To run this program, you can use GitPod/VS code editor, an online IDE. To get started, go to the GitPos  website at https://www.gitpod.io/

Once you are on the GitPad website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .js extension (e.g., NFT.js). Copy and paste the following code into the file:

```
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

var arrNTFs =[] ;

// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT(_name,_description,_color,_image,_animation_url ){
    const NFT = {
        "name":_name,
        "description":_description,
        
        "color":_color,
        "image":_image,
        "animationURL":_animation_url
    }
    arrNTFs.push(NFT);
    console.log("Minted NFT Successfully...")


}
// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function listNFTs() {
    console.log("Listing NFTs....")
    for(var i =0;i<arrNTFs.length;i++){
        const NFT = arrNTFs[i];
        console.log("ID: \t\t"+(i+1))
        console.log("Name:\t\t"+NFT.name);
        console.log("Description:"+NFT.description);
        console.log("Color:\t\t"+NFT.color)
        console.log("Image:\t\t"+NFT.image);
        console.log("Animation URL:"+NFT.animationURL);
    }

}
// print the total number of NFTs we have minted to the console
function getTotalSupply() {
    var totalSupply = arrNTFs.length
    console.log("Total supply of the NFT:"+totalSupply);
}
// call your functions below this line
mintNFT("Alen",
"This is my first NFT ever!",
"Light green",
"ipfs://bafybeiahfsvde7tjzr3rkk26ullka4w7kajxu3uisbf2yau4ud36vm257q",
"ipfs://bafybeibsxl3wfckieh6jxaj3l2icfuzwu4g5amhlgz6nh5ihip5mhuk3v4");
listNFTs();
getTotalSupply();


```
To compile the code, click on the Run Menu and select Run option in the left-hand menu bar or you can type "node NFT.js" in the Terminal.
Then you can see the O/P like  below at the Terminal.
```
Minted NFT Successfully...
Listing NFTs....
ID:             1
Name:           Alen
Description:This is my first NFT ever!
Color:          Light green
Image:          ipfs://bafybeiahfsvde7tjzr3rkk26ullka4w7kajxu3uisbf2yau4ud36vm257q
Animation URL:ipfs://bafybeibsxl3wfckieh6jxaj3l2icfuzwu4g5amhlgz6nh5ihip5mhuk3v4
Total supply of the NFT:1
```






