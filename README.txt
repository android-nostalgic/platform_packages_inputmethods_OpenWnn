-------------------------------------------------------------------------------
                            OpenWnn for Android README

                             Version 1.21-RC-20090403
                  
     (C) Copyright OMRON SOFTWARE Co., Ltd. 2008,2009 All Rights Reserved.
-------------------------------------------------------------------------------

1. About OpenWnn for Android

    OpenWnn for Android is a IME(Input Method Editor) package which
    works on Android's IMF(Input Method Framework).  This version
    contains Japanese, Chinese and English IME.

2. Contents

    This package includes the following items.

    o Document
        . Apache license paper              (text)
        . This README                       (text)
        . Change history                    (text)
        . Java docs of the IME              (HTML)

    o Building environment
        . Building control file             (XML, makefile, shell script)
        . IME native library source code    (C language)
        . IME resource                      (XML, PNG)
        . IME source code                   (Java)

3. Dictionary Libraries

  [libWnnEngDic.so: English dictionary]
      Index 0: English dictionary for normal prediction (high priority)
      Index 1: English dictionary for normal prediction (middle priority)
      Index 2: English dictionary for normal prediction (low priority)
      Index 3: English dictionary for relative prediction #1
      Index 4: English dictionary for relative prediction #2

  [libWnnJpnDic.so: Japanese dictionary]
      Index 0: Japanese dictionary for normal prediction (high priority)
      Index 1: Japanese dictionary for normal prediction (low priority)
      Index 2: Japanese dictionary for relative prediction #1
      Index 3: Japanese dictionary for relative prediction #2
      Index 4: Japanese dictionary for clause conversion (single Kanji)
      Index 5: Japanese dictionary for clause conversion (basic words)
      Index 6: Japanese dictionary for clause conversion (ancillary words)

  [libWnnZHCNDic.so: Chinese dictionary]
      Index 0: Chinese dictionary for normal prediction/conversion (high priority)
      Index 1: Chinese dictionary for normal prediction/conversion (basic words)
      Index 2: Chinese dictionary for normal prediction/conversion (single Kanji)
      Index 3: Chinese dictionary for relative prediction #1
      Index 4: Chinese dictionary for relative prediction #2

4. File constitution 

    NOTICE                                    Apache license paper
    README.txt                                This README
    ChangeLog.txt                             Change history

    doc/
      *.html                                  Java docs of the IME

    Android.mk                                Building control file
    AndroidManifest.xml                       |

    libs/                                     IME native library source code (C language)
        Android.mk                            |
        libwnnDictionary/                     |
            Android.mk                        |
            *.c                               |
            *.h                               |
            engine/                           |
                *.c                           |
            include/                          |
                *.h                           |
        libwnnEngDic/                         |
            Android.mk                        |
            *.c                               |
        libwnnJpnDic/                         |
            Android.mk                        |
            *.c                               |
        libwnnZHCNDic/                        |
            Android.mk                        |
            *.c                               |

    res/                                      IME resource (XML, PNG)
        drawable/                             |
            *.xml                             |
            *.png                             |
        layout/                               |
            *.xml                             |
        raw/                                  |
            type.ogg                          |
        values/                               |
            *.xml                             |
        values-ja/                            |
            *.xml                             |
        values-zh-rCN                         |
            *.xml                             |
        xml/                                  |
            *.xml                             |

    src/                                      IME source code (Java)
        jp/                                   |
            co/                               |
                omronsoft/                    |
                    openwnn/                  |
                        *.java                |
                        EN/                   |
                            *.java            |
                        JAJP/                 |
                            *.java            |
                        ZH/                   |
                            *.java            |
                            CN/               |
                                *.java        |

-------------------------------------------------------------------------------
