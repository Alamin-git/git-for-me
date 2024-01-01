# Git-for-me

## Git Initialize

যে folder/ডিরেক্টরি/রিপোজিটরি(repo) তে git ট্রেকেং এর কাজ করবে সেখানে git এর কার্যক্রম শুরু করতে git initialize করার জন্য....

```bash
git init
```

## Git Status

git এর বর্তমান অবস্থা/status জানতে....

```bash
git status
```

-  git status কমান্ডটি ব্যবহার করলে শুরুতে **_On branch main_** লেখা দেখতে পাওয়া যায়। এই main হলো বর্তমান ব্রাঞ্চের নাম। এবং এটাই প্রজেক্টের বর্তমান version.

## Git ADD (স্টেজিং এরিয়াতে নেওয়া)

নির্দিষ্ট কোন ফাইল স্টেজিং করতে....

```bash
git add fileName
```

লোকাল ডিরেক্টরির সব ফাইল স্টেজিং করতে....

```bash
git add --all
#or
git add -A
```

বর্তমান যে folder আছি ঐ folder এর সবকিছু স্টেজিং করতে....

```bash
git add .
```

root folder এ থাকা অবস্থায় `git add -A` এবং `git add -A` একই কথা।

## Git Commit

commit হচ্ছে ফাইনাল সিদ্ধান্ত। স্টেজে রাখা file গুলো বা file এর চেন্জেস্ গুলো ঐ অবস্থার একটি version হিসেবে গিট লোকাল রিপোতে রাখতে। কমিটের সাথে একটি অর্থপূর্ণ ম্যাসেজ ও দিতে হই। যেন পরবর্তিতে বোঝা যায় কি কারণে কমিটটা করা হয়েছিল।

```bash
git commit -m "commit message"
```

-  ফাইল স্টেজিং এরিয়াতে নেওয়ার আগে কোন কিছু কমিট করা যাবেনা বা করতে পারব না।

-  কমিট করা ফাইলে কোন পরিবর্তন করলে বা নতুন file create করলে সেই file আবার আনস্টেজ অবস্থায় চলে যায়।

-  এই অবস্থায় `git status` চেক করলে ফাইল মডিফাইড দেখাবে এবং কোন ফাইল চেন্জ করা হয়েছে সেটা দেখাবে।

-  এই পরিবর্তনকৃত ফাইল গুলোকে রাখতে হলে আবার ফাইল গুলো স্টেজে রাখতে হবে এবং ফইনাল কমিট করে git রিপোতে পাঠাতে হবে।

-  ফাইল কমিট করা হয়ে গেলে ঐ ফাইলের একটি version রিপোতে তৈরি হয়ে যায়া

-  এইভাবে প্রতিটি কমিটে git এর একটি করে version তৈরি হতে থাকবে।

## Git Log

রিপোতে করা কমিট গুলো এবং অন্যান্য ডিটেইলস্ দেখতে। এখান থেকে কমিট ম্যাসেজ এবং কমিট **_ID_** জানতে পারব।

```bash
git log
```

# H1

## H2

### H3

#### H4

##### H5

1. First ordered list item
2. Another item
   ⋅⋅\* Unordered sub-list.
3. Actual numbers don't matter, just that it's a number
   ⋅⋅1. Ordered sub-list

-  Unordered list can use asterisks
   [I'm an inline-style link](https://www.google.com)

Blocks of code are either fenced by lines with three back-ticks ```, or are indented with four spaces.

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

Three or more...

---
