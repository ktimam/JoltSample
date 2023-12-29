Jolt Physics Engine Hello World Running on ICP

Steps to Build:
  icpp build-wasm --to-compile mine
  //Install wasm larger than 2mb
  gzip ./build/joltsample.wasm
  dfx canister create joltsample
  dfx canister install joltsample --wasm ./build/joltsample.wasm.gz
  dfx canister --network local call joltsample hello '()'
  
  //Command to update canister
  dfx canister install joltsample --mode reinstall --wasm ./build/joltsample.wasm.gz
