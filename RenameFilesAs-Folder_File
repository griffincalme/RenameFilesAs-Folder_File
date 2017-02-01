# Griffin Calme 2017
# This program looks into a folder for any subfolders. It takes the name of each subfolder and inserts it into the beginning
# of each file's name within that subfolder, it then pulls the files out of the subfolder and deletes the subfolder.
# It was written to fix audiobooks that had each chapter as a folder but the files inside the chapter had non-descript naming.
# Now I can seamlessly play my books without having to manually switch to the next folder and hit play!

import os

# Please insert the path to the directory of subfolders, note the example is for Windows filesystems
path = r'C:\Users\YOUR USERNAME\MY DOCUMENTS OR WHATEVER\YOUR FOLDER OF SUBFOLDERS WITH FILES IN THEM'
subfolders = os.listdir(path)  # Generate a list of subfolders in the master folder

for subfolder in subfolders:
    try:
        files = os.listdir(path + '\\' + subfolder) # generate a list of the files in the subfolder
        for file in files:
            print(subfolder + '_' + file)
            os.rename(path + '\\' + subfolder + '\\' + file, path + '\\' + subfolder + '_' + file)

        try:
            os.rmdir(path + '\\' + subfolder)
        except:
            print('folder ' + subfolder + ' not found')
    except:
        print('subfolder + ' not found')


print('\nDone!!! ' + path)
