**Rendy™** _main_

Note :

1. Image feature only work on V130+
2. If any shape have 0 stroke, it will disappear
3. If something wrong BSOD will appear(like use image feature on unsupported version)

Config (Cell): 

1. #0 Background R(0-255)
2. #1 Background G(0-255)
3. #2 Background B(0-255)
4. #3 Shape type

Shape type(_config#3_):

1. 0 = line
2. 1 = filled rect
3. 2 = outlined rect
4. 3 = filled poly
5. 4 = outlined poly
6. 5 = image
7. 6 = Custom shape

Special flag(_bank#0_)

1. -1 = Flash config(bank#1-4>config#0-3)
2. -2 = Clear screen(Patch V1.14.33 : Start of the code will not clear screen)
3. -3 = Force flush screen(Useful for animation)

Database (Bank):

1. #0-2 Shape color(RGB) / Special flag
2. #3 Line stroke
3. #4-5 Shape XY(0-176)
4. #6-7 (_Rect_)Width and Height | (_Poly_)Sides and Radius | (_Image_)Image no. and Size
5. #8 Rotation for _poly_
6. #9 Custom shape(If _config#3_ set to 6)
