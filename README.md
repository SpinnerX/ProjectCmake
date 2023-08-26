 ____  ____   ___      _ _____ ____ _____    ____ __  __    _    _  _______ 
|  _ \|  _ \ / _ \    | | ____/ ___|_   _|  / ___|  \/  |  / \  | |/ / ____|
| |_) | |_) | | | |_  | |  _|| |     | |   | |   | |\/| | / _ \ | ' /|  _|  
|  __/|  _ <| |_| | |_| | |__| |___  | |   | |___| |  | |/ ___ \| . \| |___ 
|_|   |_| \_\\___/ \___/|_____\____| |_|    \____|_|  |_/_/   \_\_|\_\_____|
                                                                            
 _____ _____ __  __ ____  _        _  _____ _____ 
|_   _| ____|  \/  |  _ \| |      / \|_   _| ____|
  | | |  _| | |\/| | |_) | |     / _ \ | | |  _|  
  | | | |___| |  | |  __/| |___ / ___ \| | | |___ 
  |_| |_____|_|  |_|_|   |_____/_/   \_\_| |_____|
                                                  



Description

This project cmake template is how you may want to setup your project. This way it'll give an idea
on how to configure cmake. As the point is to not use glob.

NOTES
Here is why GLOB and GLOB_RECURSE should not be used (if going to be compiled by other users). It is because what GLOB does is if you GLOB a specific pattern like *.cpp for example. Then
it would just search for *.cpp in that directory. Same with GLOB_RECURSE, but recursively checks for *.cpp in the subdirectories. Now, the issue with this is what if we have .cpp files that are stray
and DO NOT want to include those .cpp files. Welp, that is why we have to explicitly tell cmake what src files to include. Or else GLOB just globally grabs those files instead. Hence, why GLOB and
GLOB_RECURSE should not be used.


ProjectCmake Purpose
Main purpose of this project is to have a generic template for cmake. Where it considers the following NOTES above. While still pertaining its use in finding the necessary source files in this project.
Just to demonstrate how this would work, including a way to include your files without typing thins like "../include/Box.h" and instead to just simply include "Box.h" or if include is called libraries name
then it would be included like: "include/Box.h".
