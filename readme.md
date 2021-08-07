# Emscripten and WebGL example

This small project demonstrates a simple application that runs as normal Desktop application as well as WASM script in the browser.

For opening the window and creating an OpenGL context, the framework GLFW is used.

The following command builds the emscripten files:

    mkdir cmake-build-emscripten
    cd cmake-build-emscripten
    emcmake cmake ..
    make
    
To start the generated WASM in the Browser, open the .html file in the cmake-build-emscripten/ folder

# Using my Flake

This requires nix 2.4, you can temporarily `nix-shell -p nixFlakes` if you have not yet upgraded to 2.4. If this is the case, ensure you pass `--experimental-features 'nix-command flakes'` to the command below.

## Remotely
`nix build github:matthewcroughan/example-emscripten-webgl#example-emscripten-webgl`

## Locally
`nix build .#example-emscripten-webgl`
