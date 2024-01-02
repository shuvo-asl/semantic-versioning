# Semantic Versioning
Practice `How to implement semantic versioning` in a project.

![Alt text](https://upload.wikimedia.org/wikipedia/commons/d/d8/SemanticVersioning.png)

### Parts of Semantic Versioning
3 parts of semantic versioning. 

* Major - Has backword incompatible
* Minor - Add new feature
* Patch - bug fix or hot fix
### Note
* Beta version always 0.1.0.
* First stable version always 1.0.0

### কি ধরনের পরিবর্তনের জন্য কোন অংশটুকু কিভাবে পরিবর্তন হবে, তার ফর্মুলা হচ্ছেঃ

যদি কোনো ধরনের Backward incompatible চেঞ্জ হয় তাহলে Major নাম্বার ১ বাড়বে, এবং Minor ও Patch নাম্বার 0 হয়ে যাবে। অর্থাৎ, আপনার আগের ভার্সন যদি 1.2.5 হয় এবং আপনার কোডে কোনও ধরনের বড় আর্কিটেকচারাল বা এমন চেঞ্জ হয় যার কারণে আগের কোডের কিছু জিনিস নতুন ভার্সনে কাজ করবে না, তাহলে এই আপডেটের পর ভার্সন নাম্বার পরিবর্তন করে 2.0.0 হবে।
যদি নতুন কোনও ফিচার বা ফাংশনালিটি যুক্ত হয় কিন্তু Backward compatible থাকে, তাহলে Minor নাম্বার ১ বাড়বে, এবং Patch নাম্বার 0 হয়ে যাবে। অর্থাৎ, আপনার আগের ভার্সন নাম্বার 1.2.5 থাকলে, আপনি যদি নতুন কোনও ফিচার যুক্ত করে রিলিজ দেন, তাহলে নতুন ভার্সন নাম্বার হবে 1.3.0
যদি কোনও বাগ ফিক্স বা হট-ফিক্স করা হয় কোডে কিন্তু Backward compatible থাকে, তাহলে শুধুমাত্র Patch নাম্বার ১ বাড়বে। অর্থাৎ আগের ভার্সন নাম্বার 1.2.5 হলে বাগফিক্সের পর ভার্সন নাম্বার হবে 1.2.6

এখান থেকে যে বিষয়টা বোঝা সবচাইতে গুরুত্বপূর্ণ তা হলো, আপনি যখন আপনার প্রজেক্টে অন্য কারও কোনো প্যাকেজ বা লাইব্রেরী(Dependency) ব্যবহার করবেন, এবং দেখবেন যে তাদের নতুন ভার্সনে Major নাম্বারটা আপডেট হয়েছে, তারমানে আপনাকে বুঝতে হবে আপনি চোখ বন্ধ করে নতুন ভার্সনে প্যাকেজ/লাইব্রেরীটা আপডেট করলে বিপদে পড়া লাগবে। এজন্য আপনাকে লাইব্রেরীটার আপডেট লগে ভালো করে দেখে নিতে হবে, নতুন আপডেটে এমন কোনো পরিবর্তন এসেছে কিনা যার কারণে আপনার কোডের কোথাও কোনো ঝামেলা হতে পারে।
কিন্তু যদি দেখেন যে কেবল মাত্র Minor নাম্বার কিংবা Patch নাম্বার আপডেট হয়েছে, তাহলে নিশ্চিন্ত মনে আপডেট করতে পারেন।

এক্ষেত্রে আরেকটা আনঅফিসিয়াল কনভেনশন ফলো করা হয়। সেটা হলো- যতক্ষণ না আপনার সফটওয়্যার/প্যাকেজ/লাইব্রেরীর একটা স্ট্যাবল প্রোডাকশন ভার্সন রেডি হচ্ছে, ততক্ষণ সেটার Major নাম্বার 0 থাকবে, অর্থাৎ ভার্সনগুলো 0.y.z এই ফরম্যাট এ থাকবে। একেবারে প্রথম ভার্সন নাম্বার হবে 0.1.0 (0.0.1 না, কারণ আপনি প্রথমে কিছু ফিচার দিয়ে রিলিজ দিবেন। প্রথমেই তো আর বাগফিক্স হবে না, তাই না? ) এবং প্রথম স্ট্যাবল প্রোডাকশন রিলিজ এর ভার্সন নাম্বার হবে 1.0.0

Semantic versioning শুধু যে লাইব্রেরী বা প্যাকেজের জন্য ব্যবহার করা হয় তা না। আপনি হয়তো Android বা iOS এপ ডেভেলপ করছেন, কিংবা কোনো API ডেভেলপ করছেন, সেখানেও আপনি এই versioning ব্যবহার করতে পারেন।
