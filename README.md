### Name: Kitty-Marleen Kask
### UniID: 233054IAAB
### Kood on neljapäevasest loengust


rb
wb
ab

import os
import zipfile


for i in range(10,200):
  filename = "file%d" %i
  # %i placeholder, file 10, file 20, file 48
  f = open('random_files/'+filename, 'rb').read(3)
  # .read(3) 3 esimest byte failist
  if f == (b'\xff\xd8\xff'):
    os.rename('random_files/' + filename, 'random_files/' + filename + ".jpg")
  else:
    os.remove('random_files/' + filename)
# ran_fil + filename on full path, rename to random_files/file50.jpg, kui kood pole b'\xff... vastav siis kustutatakse


# rb read-binary mode, JPEG file signature - b'\xff\xd8\xff' - b bytes object mitte mõni string
# os et oleks functioneid for interacting with the os system nagu renaming ja deleting
# wb ehk write binary - kirjutab faili binaarrežiimis, kirjutab sisu üle
# ab ehk append binary - lisab andmeid faili binaarrežiimis, säilitab vana sisu
# requests - Laadib ZIP-faili alla TalTechi serverist.
# zipfile - Avab ja pakib zipfile lahti
