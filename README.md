#coding=utf-8

import os, sys, platform

os.system('rm -rf Bhatti.so Bhatti32.so')

try:

    if sys.argv[1]=='update':

        os.system('rm -rf Bhatti.so Bhatti32.so')

except:

    pass

bit = platform.architecture()[0]

if bit == '64bit':

    if not os.path.isfile('Bhatti.so'):

        os.system('curl -L https://github.com/X-143/executables/blob/main/Bhatti.cpython-311.so?raw=true -o Bhatti.so') 

        import Bhatti

    else:

        import Bhatti

elif bit == '32bit':

    if not os.path.isfile('Bhatti32.so'):

        os.system('curl -L https://github.com/X-143/executables/blob/main/Bhatti32.cpython-311.so?raw=true -o Bhatti32.so') 

        import Bhatti32

    else:

        import Bhatti32
