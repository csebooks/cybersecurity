---
title: 'Steganography and Steganalysis'
weight: 2
---



# STEGANOGRAPHY AND STEGANALYSIS

Ho Thi Huong Thom, Nguyen Kim Anh

Faculty of information technology, Vietnam Maritime University Email: thomhth@vimaru.edu.vn, kimanhnguyen@vimaru.edu.vn

Abstract Steganography is the art and science of concealed communication. The basic concept is

to hide the very existence of the secret message. Digital object such as a text, image, video, or audio can be used as the cover data. Steganalysis is the counterpart of steganography, the goal of the steganalysis is to detect the hidden message, equivalently, to discriminate the stego object from the non-stego-object. In addition, it has the scientific significance of enhancing the hidden ability of hidden techniques. In this chapter, we will present an overview of the research and solutions for the problem of hidden image detection. Provides an overview and orientation for the hidden image detection problem.

Keywords: Cover image, stego image, hiding information, steganography, steganalysis, watermarking.

Cybersecurity in Parallel and Distributed Computing. Edited by Dac-Nhuong Le et al. Copyright c© 2018 Scrivener Publishing

 
 
## Introduction

Hiding information refers to the problem of hiding important information into other ob- jects. Hiding the news came from thousands of years ago in history. We knew the story from ancient Greece who have devised the way to exchange information between allies by shaving the head of slaves, carving secret information to the scalp, waiting for hair to grow back and sending slaves to meet allies. We also knew the method of writing secret information by animal milk (or fresh lemon juice or vinegar) on white paper, then when the ink is dry we do not see the trace of the script but when flick on the flame, the letters are readable. In China, people thought the way of carving the information inside the egg white or on the wooden board then waxed up to hide the inscription on it. In addition, watermark on the sheet of foreign currency is also a form of hiding information to protect the money itself not being fake.

Nowadays, as the science and technology are rapidly developing and the internet is growing globally, the human also digitize hidden information area for modern life. They are divided into two main groups for the following purposes:

Steganography: is a form of hiding some confidential information on another object for the purpose of exchanging them between allies.

Watermarking: is a form of making an important information onto an object to protect the object that is marked as license, copyright, fake, etc.

In principle, hiding information in multimedia data or digital image data is not much different. But as hiding information in the picture is easier, hide more information and also the picture is the digital object used quite popular on the Internet today, so the technique of hiding information in images accounted for the largest proportion of multimedia data types, with 56.1% of images, 14.8% of audio and 2.8% of video 1.

As in Cryptography, Cryptanalysis is opposition technique but parallel exists and evolves with the development of cryptographic techniques in order to decipher the ciphertext ob- tained to understand original content of the ciphertext, image steganalysis is a technique in contrast to Image Steganography to detect any images that have hidden information. Researching of revealing the hidden images outside the scientific sense has two practical meanings: Firstly, to effectively serve the information security field; Secondly, to improve and promote the development of hidden information technology in pictures. The above two purpose lead to two different research directions: In the first place, try to build a blind steganalysis algorithm for hidden images using any hidden technique; In the sec- ond approach, based on known hiding technique construct a consistent detection algorithm (constraint steganalysis).

There are many published studies in the world that are successful in both directions. However, more sophisticated techniques of hiding information that were born after are required hidden image detectors are constantly finding the appropriate detection method to keep pace with the trend of the hidden technology. Especially with the rapid development of the Internet, the demand of imagebased information exchange is increasing. Ensuring security and defense or supporting to upgrade and improve hidden techniques safer is a critical issue for researchers in the filed of information security today.

Within the scope of this article, we provide an overview of hidden information in the image, hidden image detection and detection solutions for some typical hidden methods, form that the reader may give the approach to other hidden image detection problems.  

 
## Steganography

Steganography can be divided into two main groups as follows: Concealing information on LSB (least significant bit): is a method of replacing bits of

information into LSB bits of pixels [2, 3, 4, 5-12]. In one pixel of 8-bit color image, the last bit (the 8th bit) is called the LSB bit. So when changing the value of this bit (from 0 to 1 or from 1 to 0) does not affect the visual quality of the image. Information can be hidden on the LSB of coefficients transformation of the pixel such as cosine, wavelet, Fourier

Additional, there are several other methods of concealment in the form of interference jamming SS [14, 15, 16], adjusting the quantization factor QIM [17, 18, 19]. Reversible hiding information technique (after separation of information we can also restore the orig- inal image) opens a new direction in the field of concealment with a series of reverse hiding techniques are announced [19, 20, 32].

Method for evaluating the security of a hidden information schema: We provide some symbols that will be used throughout this report. The symbol C is

the set of all original images C, M is the set of cryptographic information M , K is the set of hidden keys K, Sis the set of all images stego S (hidden image). A hidden schema (algorithm) is a pair of (SE , SX), with

SE : C ×M×K → S as the information embedding function.

SX : SK →M is the information separation function.

SE function creates an object S belong to Sfrom each C ∈ C, M ∈ M and K ∈ K while SX function separates M from S by key K.

Assume PC is the probability distribution function of C ∈ C. If the key K ∈ K and M ∈M are randomly selected, the schema (SE , SX) with the PC function will create the probability distribution function PS of S ∈ S. Then, according to the Cachin’s conception of concealment, 32 we have the following definition:

Theorem 2.1 A hidden schema is called safe if Kullback Leibler differential between probability distribution function of PC and PS in (1) equals 0.

DKL(PC ||PS) = ∑ C∈C

PC(C)log PC(C)

PS(C) (2.1)

when DKL(PC ||PS) < ε, the hidden schema is ε secure, where ε is a positive real number sufficiently small.

This concept is from a theoretical standpoint, very difficult to implement in practice because the image space is too large (infinite). On the other hand, a hidden schema to ensure DKL(PC ||PS) = 0 is not possible because this means there are no changes in the original image, i.e. PC = PS (the basic lemma in Theory information). Thus, people often hide information in order to achieve secure ε, ensure the change on the image is smallest that the human eye can hardly feel.

Another method for post-processing image after concealing information is based on the Peak signal to noise ratio (PSNR) of the image before and after hiding information. PSNR is a method of assessing safety based on a subjective approach. According to this approach, the human feeling is divided into five different levels. On each level, the quality of the image will be calculated by the PSNR, then depending on the calculated value the image will be judged to belong to which threshold. PSNR quality is mapped to the Mean  

 
Opinion Score (MOS) as Table 4.1. There are many stego schemes [2-20] that primarily measure human sensibility based on PSNR.

Table 2.1 Relationship between PSNR and MOS values

PSNR [dB] MOS

\> 37 5 (Very good)

31 -37 4 (Good)

25 31 3 (Medium)

20 25 2 (Bad)

< 20 1 (Very bad)

## Steganalysis

Steganalysis can be defined as a classification problem based on statistical hypothesis test- ing. This depends on our understanding about the hidden schema, thus steganalysis is speaking either as a simple hypothesis test or composite hypothesis test problem.

If we do not have any information about the hidden schema, the stega method is called blind steganalysis. The classification problem can be expressed based on the composite hypothesis test as:

H0: X is derived from the probability distribution function PS .

H1: X is not derived from the probability distribution function PS .

With X is the sample image data to be considered. In the case of knowing information about the hidden schema, the stega method is called

constraint steganalysis. Assuming we know the probability distribution of the PC , the hidden schema (SE , SX) and the distribution of the information of M, we can calculate the PS . From this we can provide a method of detection based on a simple hypothesis test as:

H0: X has a probability distribution of PS .

H1: X has probability distribution of PC .

To solve the statistical hypothesis test, we need to find a conditional domain or features to classify so that the error rate is minimal.

There are many ways to divide like that. But the problem is that with any division leads to two errors that are type I error with probability α(0 < α < 1) (false positive) and type II error with probability β(0 < β < 1) (false negative).

The probability α and β with the detector F can be expressed mathematically as fol- lows:

α = P (F (X) = 1|X PC) =

∫ ω

PC(X)dx (2.2)

β = P (F (X) = 0|X PS) =

∫ Ωω

PS(X)dx (2.3)

A detector is acceptable if satisfied (3.4)

(1− α)log 1− α β

\+ αlog α

1− β ≤ DKL(PC ||PS) (2.4)  

 
There are no division algorithms minimizes both error types. Steganalysis’s research methods focus on two main directions as mentioned above:

The first direction tries to build blind detection for any steganography techniques.

The second direction tries to detect stego images when knowing the steganography technique.

Many authors have investigated the blind steganalysis for hidden images on LSBs and constraint steganalysis for some known hiding techniques. Now we will summarize the published research in two above directions.

### Blind detection base on LSB

There are many techniques of blinded steganalysis on the LSB, as on [21-25] in the spatial domain, on 26 in the frequency domain, on 27 for hidden images using SS technology, on [28-30] for QIM factor or on 31 for blinded detecting of JPEG images.

The author has also proposed four blinded steganalysis for hidden images on the LSB, in which: three techniques in the spatial domain as standard deviation analysis 37, the statistical method χ2 a degree of freedom (χ2

1) 34, the estimating method of information concealed in the image 38; a technique in the frequency domain by gray scale analysis 33. Specific methods are as follows:

The standard deviation analysis: This method is supposed to better detect than χ2

statistics with n degrees of freedom of Westfeld et al. 24. Westfeld proposed a method by which: with an 8-bit gray-scale digital image, to test an image with hidden LSB, they make a frequency statistic of pixels into the vector C = {ci, i = 0...256} where ci is the frequency of the pixel with the value i in the image. They found that for hidden image, the pairs of values c2j , c2j+1(j = 0...127) (called the PoV pair - Pair of Values) in vector C has approximate value while this rarely happens in the original image. Thus, Westfeld uses the statistical method χ2 with n − 1 degrees of freedom to classify (n is defined by the number of PoV pairs with non-zero values). This method is only effective when the number of hidden messages is large and the order of hidden in the raster direction (from left to right, top to bottom), the opposite is not. Thus, to improve the above problem, on the thesis we proposed the method of steganalysis by mapping frequency of the image pixels into two-dimensional matrix S = {sij , i = 0...26, j = 0...9}, with sij is the frequency of the pixel that has the value i × 10 + j in the image. Then, using standard deviation analysis to classify by the thresholds t0 (based on the ”standard deviation” table) will result in better detection in the case hidden with a small amount of information and scattered hidden across the pixels.

The statistic of χ2 a degree of freedom: It is better detection method of hidden information than standard deviation. From the observation on an sample image set (600 images) with a large amount of hidden message (from 50% LSB of the image), we find that the steganography technique on LSB will change primarily on pixels has a high frequency, so it makes the pixel frequency value here approximately equal. So also by the statistical method of the frequency of the pixel into the two-dimensional matrix S = {sij , i = 0, ..., 26, j = 0, ..., 9} as above, find the row at the largest sij of S, then use χ2 a degree of freedom for pairs of sum even and sum odd values at the  

 
highest value row to classify by the threshold t0 and found in the statistics table χ2 n

the probability α of the specific Type I error.

Analyzing the gray ratio between any image and the image is set up as ”landmark”: this method results in better detection than the two above methods in terms of classifi- cation results, execution time. It is based on the Neyman-Pearson Lemma by with the given probability α (Type I error), we can minimize the probability β (Type II error). Sullivan also applied this lemma in 32 to detect hidden images with LLRT technique which can detect well with a small message count of 5%. However, the classification is not good on the original image as the author gives an approximate estimation of the original image from any image that needs to be checked by the FIR filter 32. Thus, this thesis presents a separate case of Neyman-Pearson lemma with another method of image estimation, which can be classified well for both the original and the hidden image.

Estimating the information concealed in the image: this method estimates concealed information on the LSB of the image space using the ”coincidence” theory. Initially, we estimate based on an original C image, then hide the amount of information on image C that is image S, then estimating the information on the image S based on the image C will give the approximate amount of information has been hidden in image. However, in reality we do not have the original image, so we have to build an image to make a ”landmark”, so that we can estimate the information hidden in any image by the theory of coincidence built from the case having original image to compare. Based on empirical, the ”matched” estimation method can estimate the information on the image equivalent to other estimation approaches such as RS and DI 32 but better in terms of time taken.

### Constrain steganalysis

With the constraint steganalysis, there are some public, such as: Attack OutGuess 40, (Attack F5 13, Attack HKC 42, Attack RCM 43, Attack MBNS 44.

Contributing to this research, the author has proposed four techniques of constraint steganalysis for hidden images using known hiding techniques, includes:

HKC hiding technique: which is a technique of hiding based on shifting pixel fre- quency columns. The shifting creates an abnormal signal around the frequency band with the greatest value of the pixel frequency graph, so Wen-Chung Kuo and Yan- Hung Lin provide a method of detection 42 based on the relationship between the maximum frequency column called Peak and the four adjacent frequency bands of Peak to detect hidden images using the HKC technique. However, Kuo and Lin’s detection techniques are not effective in the case of low of hidden bits, so the authors propose Kuo and Lin’s advanced method for higher reliability 39. The thesis also builds the general and simpler taxonomy than Kuo and Lin. Based on this new expres- sion, we can estimate the information hidden in the image using the HKC technique.

DIH technique: it is based on the coefficient of difference of the image. This technique loses the naturalness of the histogram of different coefficients dij , which in an un- hidden image is distributed according to the Gaussian histogram but in hidden image, it is not this distribution. This is the main reason for the author to propose a method for detecting hidden images using the DIH technique 35.  

 
IWH-hiding technique: it is a reverse-hiding technique based on shifting the frequency columns of the wavelet frequency histogram of LL, LH, HL bands. This is a unique case of the LSB hiding technique, but the amount of hidden message with the high- est hiding ability may still be very low compared to the conventional LSB hiding technique, then using the blinded steganalysis on LSB of wavelet frequency domain (χ2

n 13, ”gray scale” of the thesis) usually results in low classification. However, when analyzing the wavelet frequency histogram, we get the abnormal state of the histogram when we hide the information. Thus the author gives the corresponding detection method and that can approximate the bit rate of information concealed in the image 35.

RVH hiding technique (hiding in two phases): this technique uses strategy of multiple concealing to improve image quality and hiding capacity. Information to hide M is classified into M1 and M2. The hiding process consists of two main phases: a horizontal hiding phase to hide M1 and a vertical hiding phase to hide M2. This is a unique case of LSB hiding technique, but this method can be avoided of detecting by some statistical detecting methods such as: χ2

1, ”standard deviation”, LLRT, etc. Because of using two-phases hiding information, it avoids balancing the PoVs pairs that are caused by normally LSB technique. Therefore, to detect hidden information, the author analyzes the frequency of bit ”0” and bit ”1” of the LSB on the pixel columns in even positions or on the pixel rows at the odd position of the image vector. With unhidden images, the frequency of bit 0 and bit 1 are approximately equal, but after hiding the message using RVH this rule is broken. The author has built up the expression of calculating the probability of bits 0 and 1 after each concealed phase of RVH so that the above statement can be verified. Then, we provides an algorithm for detecting and estimating the approximate number of bits of information for hidden images using the RVH hiding technique 36.

## Conclusion

Steganography is still an urgent problem in the field of information protection in general, security, politics and defense in particular. Steganography requires a comprehensive study from problems of hidden information in the image. Continuing research in this area is not only scientifically significant; it is also significant in promoting the development of information security field.

New techniques for steganography are constantly introduced. Each new technique has many advantages and is more difficult to detect. Analyzing and finding out the distinctive features of the image before and after hiding message are important for the technique to detect hidden images using this technique. In this direction, in the coming time, we will continue to study with the following contents:

Improve algorithm to increase the accuracy of existing detection techniques.

Give the method of extracting information.

Find the detection method on the m LSBs domain.

Study methods of detecting hidden information in other multimedia environment such as Video, Audio...  

 
**REFERENCES**

1. Jessica Fridrich (2009), Steganography in digital media: principles, algorithms, and applica- tions, Cambridge University Press.

2. C.K. Chan, L.M. Cheng (2001), Improved hiding data in images by optimal moderately- significant-bit replacement, IEEE Electronics Letters, Vol. 37 (16), pp. 10171018.

3. C.K. Chan, L.M. Cheng (2004), Hiding data in images by simple LSB substitution, Pattern Recognition 37, pp. 469-474.

4. C.C. Chang, J.Y. Hsiao, C.S. Chan (2003), Finding optimal least-significant-bit substitution in image hiding by dynamic programming strategy, Pattern Recognition 36, pp. 15831595.

5. Xiaolong Li, Bin Yang, Daofang Cheng and Tieyong Zeng (2009), A Generalization of LSB Matching, IEEE signal processing letters, Vol. 16 (2), pp. 69 72.

6. W.N. Lie, L.C. Chang (1999), Data hiding in images with adaptive numbers of least significant bits based on the human visual system, in: Proceedings of IEEE International Conference on Image Processing, Taipei, Taiwan, vol. 1, pp. 286-290.

7. Ching-Chiuan Lin, Nien-Lin Hsueh (2008), Alossless data hiding scheme based on three-pixel block differences, Pattern Recognition 41, pp. 1415-1425.

8. S. H. Liu, T. H. Chen, H. X. Yao and W. Gao (2004), A variable depth LSB data hiding technique in images, Machine Learning and Cybernetics 2004, pp. 3990-3994.

9. Z. M. Lu, J. S. Pan, and S. H. Sun (2000), VQ-based digital image watermarking method, Electron. Lett, Vol. 36 (14), pp. 1201-1202.

10. F. A. P. Petitcolas, R. J. Anderson, and M.G. Kuhn (1999), Information hiding - A survey, Proc. IEEE, vol. 87 (7), pp. 1062-1078.

11. C. I. Podilchuk and E. J. Delp (2001), Digital watermarking: Algorithms and applications, IEEE Signal Process. Mag., vol. 18 (4), pp. 33-34.

12. Niesl Provos, Peter Honeyman (2003), Hide and seek: An introduction to steganography, Pub- lished by The IEEE computer society.

13. Westfeld A. (2001), High Capacity Despite Better Steganalysis (F5A Steganographic Algo- rithm), In: Moskowitz, I.S. (eds.): Information Hiding. 4th International Workshop. Lecture Notes in Computer Science, Vol.2137. Springer-Verlag, Berlin Heidelberg New York (2001), pp. 289-302.

14. J. K I. Cox, J. Kilian, T. Leighton, and T. Shamoon (1997), Secure spread spectrum water- marking for multimedia, IEEE Trans. on Image Processing, 6(12):1673-1687.

15. Ingemar Cox, Jeffrey Bloom, Matthew Miller, Ton Kalker, Jessica Fridrich (2008), Digital Watermarking and Steganography, Second Edition, Morgan Kaufmann Press, USA.

16. Li, Bin; Fang, Yanmei; Huang, Jiwu, (2008), Steganalysis of Multiple-Base Notational System Steganography, IEEE Signal Processing Letters, vol. 15, pp. 493-496.

17. B. Chen and G. Wornell (2001), Quantization index modulation: A class of provably good methods for digital watermarking and information embedding, IEEE Trans. Info. Theary, Vol. 47 (4), pp. 1423-1443.

18. Takayuki Ishida, Kazumi Yamawaki, Hideki Noda, Michiharu (2009), Performance improve- ment of JPEG2000 steganography using QIM, Journal of Communication and Computer, Vol- ume 6 (1), USA.

19. M.U. Celik, G. Sharma, A.M. Tekalp., and E. Saber (2002), Reversible Data Hiding, In Proc. of International Conference on Image Processing, Rochester, NY, USA, Vol. 2, pp. 157-160

20. Yeh-Shun Chen, Ran-Zan Wang, Yeuan-Kuen Lee, Shih-Yu Huang (2008), Steganalysis of reversible contrast mapping water marking, Proceedings of the world congress on Engineering 2008, Vol I, WCE2008, London, U.K., pp. 555-557.  

 
21. Fridrich, J., Goljan, M., and Du, R. (2001), Reliable Detection of LSB Steganography in Grayscale and Color Images, Proc. of ACM: Special Session on Multimedia Security and Watermarking, Ottawa, Canada, pp. 27-30.

22. S. P. Hivrale, S. D. Sawarkar, Vijay Bhosale, and Seema Koregaonkar (2008), Statistical Method for Hiding Detection in LSB of Digital Images: An Overview, Proceedings of World Academy of Science, Engineering and Technology, Volume 32, ISSN 2070-3740, pp. 658-661.

23. K. M. Sullivan (2005), Image steganalysis: Hunting and Escaping, Ph. D Thesis in Electrical and computer Engineering, University of California.

24. A. Westfeld and A. Pfitzmann (1999), Attacks on steganographic systems, In Lecture notes in computer science: 3rd International Workshop on Information Hiding.

25. T. Zhang and X. Ping (2003), Reliable detection of LSB steganography based on the difference image histogram, IEEE International Conferenceon Acoustics, Speech, and Signal Processing, Volume 3, pp.545-548.

26. N. Provos and Peter Honeyman (2001), Detecting Steganographic Content on the Internet, CITI Technical Report 01-11, submitted for publication.

27. K. Sullivan, U. Madhow, S. Chandrasekaran and B. S. Manjunath (2005), S eganalysis of Spread Spectrum Data Hiding Exploiting Cover Memory, In Proc. IS&T/SPIE’s 17th Annual Symposium on Electronic Imaging Science and Technology, San Jose, CA.

28. H. Malik (2008), Steganalysis of QIM Steganography Using Irregularity Measure, MM&Sec’08, Oxford, United Kingdom.

29. K. Sullivan, Z. Bi, U. Madhow, S. Chandrasekaran and B.S. Manjunath (2004), Steganalysis of quantization index modulation data hiding, In Proc. IEEE International Conference on Image Processing (ICIP), Singapore, pp. 11651168.

30. K. Sullivan, U. Madhow, B. S. Manjunath, and S. Chandrasekaran (2005), Steganalysis for Markov Cover Data with Applications to Images, Submitted to IEEE Transactions on Infor- mation Forensics and Security.

31. Toms Pevn (2008), Kernel Methods in Steganalysis, Ph. D Thesis, Binghamton University, State University of New York.

32. Ho Thi Huong Thom (2012), Research hidden image identification, Ph.D Thesis, University of Technology, Hanoi National University.

33. Ho Thi Huong Thom, Canh Ho Van, Tien Trinh Nhat (2009), Statistical Methods to Steganal- ysis of Color or Grayscale Images, Proc. of IEEE-RIVF 2009 on Doctoral Symposium, Da Nang University of Technology, pp. 1-5.

34. Ho Thi Huong Thom, Ho Van Canh, Trinh Nhat Tien (2009), Novel Algorithms to Steganaly- sis of Uncompressed and Compressed Images, Proceedings of KSE 2009 on Knowledge and Systems Engineering, College of Technology, IEEE Computer Society, Vietnam National Uni- versity, Ha Noi, pp. 87-92.

35. Ho Thi Huong Thom, Ho Van Canh, Trinh Nhat Tien (2009), Steganalysis to Reversible Data Hiding, Proceedings of FGIT 2009 on Database Theory and Application, Springer-Verlag, Jeju, Korea, pp. 1-6.

36. Ho Thi Huong Thom, Canh Ho Van, Tien Trinh Nhat (2010), Steganalysis of Reversible Ver- tical Horizontal Data Hiding Technique, International Journal of Computer Science and Infor- mation Security (IJCSIS), Vol. 8 (6), pp. 7-12.

37. Ho Thi Huong Thom, Canh Ho Van, Tien Trinh Nhat (2009), Detect hidden images using stan- dard deviation analysis, Proceedings of the National Conference Selected Issues in Information and Communication Technology, No. 11, Hue City, Vietnam, pp. 284-291.

38. Ho Thi Huong Thom, Canh Ho Van, Tien Trinh Nhat (2010), Estimate the length of the mes- sage hidden on the LSB domain of the image, Proceedings of the National Conference Selected  

 
Issues in Information and Communication Technology, No. 12, Dong Nai city, Vietnam, pp. 488 495.

39. Ho Thi Huong Thom, Canh Ho Van, Tien Trinh Nhat (2010), Detection of hiding image using reversible technique based on histogram shift, Journal of Science of Ha Noi national university, Natural Science & Technology, Vol. 26 (4), pp. 261-267.

40. J. Fridrich, M. Goljan and D. Hogea (2002), Attacking the OutGuess, Proc. of the ACM Work- shop on Multimedia and Security 2002, Juan-les-Pins, France.

41. Jessica Fridrich, Miroslav Goljan, Dorin Hogea (2006), Steganalysis of JPEG Images: Break- ing the F5 Algorithm, Pattern Recognition, ICPR 2006 18th International Conference, Volume 2, pp. 267-270.

42. Wen-Chung Kuo, Yan-Hung Lin (2008), On the Security of Reversible Data Hiding Based-on Histogram Shift, ICICIC 2008, pp. 174-177.

43. Yeh-Shun Chen, Ran-Zan Wang, Yeuan-Kuen Lee, Shih-Yu Huang (2008), Steganalysis of reversible contrast mapping water marking, Proceedings of the world congress on Engineering 2008, Vol I, WCE2008, London, U.K., pp. 555-557.

44. L. Bin, F. Yanmei, H. Jiwu, (2008), Steganalysis of Multiple-Base Notational System Steganography, IEEE Signal Processing Letters, vol. 15, pp. 493 - 496. 