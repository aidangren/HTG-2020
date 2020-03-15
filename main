#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Created on Sun Mar 15 10:29:14 2020

@author: Aidan
"""

from ipywidgets.embed import embed_minimal_html
from PIL import ImageFilter
import gmaps
gmaps.configure(api_key="AIzaSyCo99awBRG0JvRCoJC8M12-3EiAoLfElSM")
fig = gmaps.figure()
#center=(36.000958, 68.642370),zoom_level=16,map_type='HYBRID'
from PIL import Image
im = Image.open("/Users/Aidan/36.070403, 68.629560, 68.673354.png")
inputim=im.filter(ImageFilter.ModeFilter(8))
inputim.show()
pix=inputim.load()
imout = im.copy()
pixout=imout.load()
deltax=68.673354-68.629560
locations=[]
xlist=[]
ylist=[]
for i in range(0,inputim.size[0],8):   #x-axis search
    for j in range(0,inputim.size[1],8): #y-axis search
        #for x2 in range (0,4):
        #    for y2 in range (0,4):
        #        plist=plist+[pix[i+x2,j+y2][1]]
        if pix[i,j][1] > 140:
        #    for x3 in range (0,4):
        #        for y3 in range (0,4):
                    pixout[i,j]= (255,0,0)
                    xlist=xlist+[-j/1000*delta+36.070403]
                    ylist=ylist+[i/1000*delta+68.629560]
            #ycall=ycall+1
            #if ycall > 10: #size clumping
            #    k=1;
            #    for x2 in range(i-3,i+3):
            #        if x2<0:
            #            x2=1;
            #        elif x2>im.size[0]:
            #            x2=im.size[0]
            #        if pix[x2,j][1] < 140:
            #            k=0;
            #    if k==1:
            #        for x3 in range(i-3,i+3): #x-axis search
            #            for y3 in range(j-ycall,j): #y-axis sear
for k in range(0,len(xlist),5):
    locations=locations+[(xlist[k],ylist[k])]
#print(locations)
imout.show()
marker = gmaps.marker_layer(locations)
fig.add_layer(marker)
embed_minimal_html('export3.html', views=[fig])
