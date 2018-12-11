import glob
import cv2
files = sorted(glob.glob(r"F:/test/n000001/*.jpg")) # .jpgのみ列挙
for f in files:

  img = cv2.imread(f)
  print(img.shape)
