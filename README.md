# Teramux-zip-crack-real-working

​🛠️ সম্পূর্ণ শুরু থেকে শেষ: জিপ ক্র্যাকিং মাস্টার গাইড

​১. প্রয়োজনীয় প্যাকেজ ইনস্টল করা (একদম প্রথমে)

​টার্মাক্স ওপেন করে প্রথমে পাইথন এবং গিট ইনস্টল করে নিতে হবে। এই কমান্ডটি দিয়ে এন্টার দাও:

pkg install git python -y

2.Pydictor টুলটি নামানো ও সেটআপ করা

​এবার গিটহাব থেকে পাসওয়ার্ড লিস্ট তৈরির মেইন টুলটি ক্লোন করে ফোল্ডারের ভেতর ঢুকতে হবে:

git clone https://github.com/LandGrey/pydictor.git
cd pydictor

আইডিয়া ১: যদি শুধু সংখ্যা মনে হয় (যেমন: ৪ থেকে ৬ ডিজিটের পিন)


python pydictor.py -base d --len 4 6 -o list.txt

আইডিয়া ২: যদি অক্ষর ও সংখ্যা মেশানো মনে হয় (যেমন: rahul123)


python pydictor.py -base dL --len 5 8 -o list.txt



আইডিয়া ৩: কাস্টম কিছু সংখ্যা/অক্ষর ফিক্সড মনে থাকলে (যেমন: abc12)

python pydictor.py -char abc12 -o list.txt


৪. জিপ ফাইলটি সঠিক জায়গায় রাখা

​তোমার যে জিপ ফাইলটি লক করা আছে (যেমন: game.zip), সেটিকে তোমার ফোনের ফাইল ম্যানেজার ব্যবহার করে এই pydictor ফোল্ডারের ভেতরে এনে পেস্ট করে রেখে দেবে।

​৫. পাইথন ক্র্যাকিং স্ক্রিপ্ট চালানো (মেইন কাজ)

​সব সেটআপ শেষ হলে, নিচের এই পুরো কোডটি হুবহু কপি করে টার্মাক্সে পেস্ট করে এন্টার দেবে।

​⚠️ মনে রেখো: তোমার জিপ ফাইলের নাম যদি game.zip না হয়ে অন্য কিছু হয়, তবে স্ক্রিপ্টের ৩ নম্বর লাইনে 'game.zip' কেটে তোমার ফাইলের আসল নামটা বসাবে।


python3 -c "
import zipfile
import os

zip_file = 'game.zip'
wordlist = 'results/list.txt'

if not os.path.exists(zip_file):
    zip_file = '../' + zip_file

if not os.path.exists(zip_file):
    print('[-] Error: জিপ ফাইলটি খুঁজে পাওয়া যায়নি! সঠিক ফোল্ডারে রাখুন।')
else:
    print('[*] Cracking started... Please wait...')
    found = False
    with open(wordlist, 'rb') as f:
        for line in f:
            password = line.strip()
            try:
                with zipfile.ZipFile(zip_file) as zf:
                    zf.extractall(pwd=password)
                    print(f'\n[+] SUCCESS! PASSWORD FOUND: {password.decode()}')
                    found = True
                    break
            except Exception as e:
                continue
    if not found:
        print('\n[-] দুঃখিত মামা, এই লিস্টের কোনো পাসওয়ার্ডই মিলল না।')
"


৬. আনজিপ হওয়া ফাইল দেখা
​স্ক্রিপ্টটি সাকসেসফুল হলে পাসওয়ার্ড স্ক্রিনে দেখাবে এবং ফাইল আনজিপ হয়ে যাবে। ফাইলগুলো দেখতে এই কমান্ডটি দেবে:

ls




