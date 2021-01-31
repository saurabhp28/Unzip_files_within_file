# Unzip_files_within_file


from zipfile import ZipFile
import os 

for n in range(<max_number>,-1,-1):     #say we need to unzip, 50.zip, giving us 49.zip....
	if n < 10:
		zip_file = '0'+str(n)+'.zip'
	else:
		zip_file = str(n)+'.zip'

	print(zip_file)
	password = 'pass'

	with ZipFile(zip_file) as zf:
		zf.extractall(pwd=bytes(password,'utf-8'))
