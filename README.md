# ic-mnist

1. The frontend provides a canvas where users can draw a digit. 
2. The drawn digit is then sent to the backend canister running `burn-rs` for inference using a pretrained MNIST model. 
3. The backend performs the inference and returns the predicted digit to the frontend.

# Installation 

To set up the project, follow these steps:
0. Have Rust and Nodejs installed.
1. Installl [IC-SDK](https://github.com/dfinity/sdk/) (building from `master` branch because we need `gzip` feature which is not available in the latest release) 
``` bash
git clone https://github.com/dfinity/sdk.git ./ic-sdk
cargo build --manifest-path=ic-sdk/Cargo.toml -p dfx
```
2. Clone and deploy this project
``` bash
git clone https://github.com/smallstepman/ic-mnist.git ./ic-mnist
cd ic-mnist
../ic-sdk/target/debug/dfx start --background --clean
../ic-sdk/target/debug/dfx deploy
```

# License
The code in this repository is licensed under the MIT License.

# Acknowledgements
Based on `burn` (https://burn-rs.github.io), backend and frontend implementation copied from this example https://github.com/burn-rs/burn/tree/main/examples/mnist-inference-web, 


