 This features a Non Fungible Token (NFT) module. The module allows the collection manager 
    to mint NFTs and withdraw NFT sales, allows users to combine two NFTs into a new NFT and burn 
    NFTs.

    Collection manager
        The collection manager is the owner of the MinterCap object. The collection manager can mint
        NFTs and withdraw NFT sales.

    Minting NFTs
        In this module, NFTs are minted by the manager of the collection. Minting an NFT requires a
        payment of 1 SUI, which is sent to the MinterCap object. Any change is returned to the 
        sender of the transaction. The NFT is then transferred to the recipient. The NFT is 
        represented by the NonFungibleToken object.

    Combining NFTs
        Anyone that owns two or more NFTS can combine two NFTs into a new NFT. The two NFTs are 
        deleted and a new NFT is created and returned to the sender of the transaction. The new NFT 
        is represented by the NonFungibleToken object.

        When combining two NFTs, the name of the new NFT is the concatenation of the names of the
        two NFTs. For example, 
            - NFT1 name: "NFT1"
            - NFT2 name: "NFT2"
            - New NFT name: "NFT1 + NFT2"
        
        The description of the new NFT is as follows: 
            - "Combined NFT of " + NFT1 name + " and " + NFT2 name

        For example, 
            - NFT1 name: "NFT1"
            - NFT2 name: "NFT2"
            - New NFT description: "Combined NFT of NFT1 and NFT2"

        The new NFT image url will be provided by the sender of the transaction.

    Burning NFTs
        Anyone that owns an NFT can burn it. The NFT is deleted.

    Withdrawing NFT sales
        THe collection manager can withdraw the sales balance from the MinterCap object. The sales
        balance is the total amount of SUI that has been paid for NFTs. 

    Public Getters
        The module provides public getters for the name, description and image of an NFT. This can 
        be called by anyone on any existing NFT.
