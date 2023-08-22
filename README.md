# precompiled_sdl2 by Kribz1k -> Go to "Code" above to view readme!

// I've precompiled SDL2 for people to use with Windows OS and Visual Studio
// To use: Drag the contents of the "SDL 2.28.2 Premade by Kribz1k" folder to your project directory
// For x64 use
// Tested on Windows 11 using Visual Studio

You can use these steps and the code below to test SDL successfully runs for your project:
1. Adding "include" and "lib" directories: right-click solution > properties > VC++ > Include Directories (add include folder location) + Library Directories (add lib folder location) 
2. Adding SDL2.lib and SDL2main.lib dependencies: right-click solution > properties > Linker > Input > Additional Dependencies > Type: SDL2.lib; SDL2main.lib;
3. Placing SDL2.dll in the root of your project directory

#include <iostream>
#include <SDL.h>

using namespace std;

int SDL_main(int argc, char* argv[])
{
    if (SDL_Init(SDL_INIT_VIDEO) < 0)
    {
        // Handle initialization error
        cout << "SDL initialization failed..." << endl;
        return 1;
    }

    cout << "SDL initialization succeeded..." << endl;

    // Your SDL code and event loop here

    SDL_Quit();
    return 0;
}
