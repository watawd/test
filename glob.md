import glob
import cv2
files = sorted(glob.glob(r"F:/test/n000001/*.jpg")) # .jpgのみ列挙
for f in files:

  img = cv2.imread(f)
  print(img.shape)


from PIL import Image
import numpy
pil = Image.open("lena.jpg").convert("RGB")#RGBAに変換
imgArray = numpy.asarray(pil)
print(imgArray)


import cv2
from PIL import Image
import numpy as np
im_pillow = np.array(Image.open('lena.jpg'))
    im_bgr = cv2.cvtColor(im_pillow, cv2.COLOR_RGB2BGR)
    Image.fromarray(im_bgr).save('lena_cv2.jpg')
    cv2.imwrite('lena_cv2.jpg', im_bgr)
    im = np.array(Image.open('lena_cv2.jpg'))
    print(im.shape)
    cv2.imshow("cv2", im)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
