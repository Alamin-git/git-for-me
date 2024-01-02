# <span style="color:DodgerBlue"> **Git for me**</span>

-  [Git Initialize](#git-initialize)
-  [Git Status](#git-status)
-  [Git Add](#git-add-স্টেজিং-এরিয়াতে-নেওয়া)
-  [Git Commit](#git-commit)
-  [Git Log](#git-log)
-  [Git Branch](#git-branch)

## <span style="color:CornflowerBlue">Git Initialize</span>

**যে folder/ডিরেক্টরি/রিপোজিটরি(repo) তে git ট্রেকিং এর কাজ করবে সেখানে git এর কার্যক্রম শুরু করতে git initialize করার জন্য...**

```bash
git init
```

## <span style="color:CornflowerBlue">Git Status</span>

**git এর বর্তমান অবস্থা/status জানতে...**

```bash
git status
```

> -  git status কমান্ডটি ব্যবহার করলে শুরুতে **_On branch main_** লেখা দেখতে পাওয়া যায়। এই main হলো বর্তমান ব্রাঞ্চের নাম। এবং এটাই প্রজেক্টের বর্তমান version.

## <span style="color:CornflowerBlue">Git Add</span> (স্টেজিং এরিয়াতে নেওয়া)

**নির্দিষ্ট কোন ফাইল স্টেজিং করতে...**

```bash
git add fileName
```

**লোকাল ডিরেক্টরির সব ফাইল স্টেজিং করতে...**

```bash
git add --all
#or
git add -A
```

**বর্তমান যে folder আছি ঐ folder এর সবকিছু স্টেজিং করতে...**

```bash
git add .
```

> -  root folder এ থাকা অবস্থায় `git add -A` এবং `git add -A` একই কথা।

## <span style="color:CornflowerBlue">Git Commit</span>

**commit হচ্ছে ফাইনাল সিদ্ধান্ত। স্টেজে রাখা file গুলো বা file এর চেন্জেস্ গুলো ঐ অবস্থার একটি version হিসেবে গিট লোকাল রিপোতে রাখতে। কমিটের সাথে একটি অর্থপূর্ণ ম্যাসেজ ও দিতে হই। যেন পরবর্তিতে বোঝা যায় কি কারণে কমিটটা করা হয়েছিল।**

```bash
git commit -m "commit message"
```

> -  ফাইল স্টেজিং এরিয়াতে নেওয়ার আগে কোন কিছু কমিট করা যাবেনা বা করতে পারব না।
> -  কমিট করা ফাইলে কোন পরিবর্তন করলে বা নতুন file create করলে সেই file আবার আনস্টেজ অবস্থায় চলে যায়।
> -  এই অবস্থায় `git status` চেক করলে ফাইল মডিফাইড দেখাবে এবং কোন ফাইল চেন্জ করা হয়েছে সেটা দেখাবে।
> -  এই পরিবর্তনকৃত ফাইল গুলোকে রাখতে হলে আবার ফাইল গুলো স্টেজে রাখতে হবে এবং ফইনাল কমিট করে git রিপোতে পাঠাতে হবে।
> -  ফাইল কমিট করা হয়ে গেলে ঐ ফাইলের একটি version রিপোতে তৈরি হয়ে যায়া
> -  এইভাবে প্রতিটি কমিটে git এর একটি করে version তৈরি হতে থাকবে।

**একটি কমিট থেকে অন্য কমিটে যেতে চাইলে...**

> -  কোন ফাইল বা ফোল্ডার আনকমিট অবস্থায় থাকলে চেক আউট করতে পারব না।

```bash
git checkout commitId
```

**লাষ্ট ভার্সন বা লাষ্ট কমিটে বা main virsion এ ফিরে যেতে...**

```bash
git checkout main
```

## <span style="color:CornflowerBlue">Git Log</span>

**রিপোতে করা কমিট গুলো এবং অন্যান্য ডিটেইলস্ দেখতে। এখান থেকে কমিট ম্যাসেজ এবং কমিট **_ID_** জানতে পারব...**

```bash
git log
```

**সুন্দর কম্প্যাক ভার্সনে ছোট করে প্রয়োজনীয় সব দেখতে...**

```bash
git log --oneline
```

## <span style="color:CornflowerBlue">Git Branch</span>

**নতুন ব্রাঞ্চ তৈরি করতে...**

> -  যেই ব্রাঞ্চ থেকে নতুন ব্রাঞ্চ তৈরি করা হবে। নতুন ব্রাঞ্চ ঐ ব্রাঞ্চেরই একটি কপি হিসেবে তৈরি হবে।
> -  ব্রাঞ্চকেও একটি ভার্সন হিসেবে ধরা যেতে পারে।

```bash
git branch branchName
```

**এক ব্রাঞ্চ থেকে অন্য ব্রাঞ্চে প্রবেশ করতে...**

```bash
git checkout branchName
#or
git switch branchName
```

**নতুন ব্রাঞ্চ তৈরি করে সাথে সাথে সেই ব্রাঞ্চে প্রবেশ করতে...**

```bash
git checkout -b branchName
```

**প্রজেক্টে থাকা সবগুলো ব্রাঞ্চের লিস্ট দেখতে...**

```bash
git branch
#or
git branch --list
```

**কোন ব্রাঞ্চ ডিলিট করতে...**

```bash
git branch -D branchName
```

> -  ব্রাঞ্চে কোন মোডিফিকেশন থাকলে সেটাও ডিলিট হয়ে যাবে।
> -  তবে যদি `-D` এর পরিবর্তে `-d` দেওয়া হয় তাহলে ঐ ব্রাঞ্চে কিছু আনকমিট থাকলে গিট warning দিবে।
