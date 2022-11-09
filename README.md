# Graph NFT Marketplace FCC

This project is a part of the Hardhat FreeCodeCamp video.

_[ :movie_camera: FreeCodeCamp video](https://www.youtube.com/watch?v=gyMwXuJrbJQ&t)_

If you want to know more about this project go to the FreeCodeCamp original repo

_[ :classical_building: FreeCodeCamp original repo](https://github.com/PatrickAlphaC/graph-nft-marketplace-fcc)_

# Demo

https://nextjs-nft-marketplace-thegraph-fcc.vercel.app/

# Quickstart

1. Install Subgraph CLI

```
yarn global add @graphprotocol/graph-cli
```

2. Log into [the graph UI](https://thegraph.com/studio/subgraph) and create a new Subgraph.

Use Goerli as the network.

3. Initialize Subgraph

```
graph init --studio nft-marketplace
```

4. Authenticate CLI

```
graph auth  --studio YOUR_DEPLOY_KEY_HERE
```

5. Update your `subgraph.yaml`

- Update the `address` with your NftMarketplace Address
- Update the `startBlock` with the block right before your contract was deployed

6. Build graph locally

```
graph codegen && graph build
```

- `graph codegen`: Generates code in the `generated` folder based on your `schema.graphql`
- `graph build`: Generates the build that will be uploaded to the graph

7. Deploy subgraph

Replace `VERSION_NUMBER_HERE` with a version number like `0.0.1`.

```
graph deploy --studio nft-marketplace -l VERSION_NUMBER_HERE
```

8. View your UI

Back in your hardhat project, mint and list an NFT with:

```
yarn hardhat run scripts/mint-and-list-item.js --network goerli
```
