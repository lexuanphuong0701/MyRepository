# MyRepository
/home/phuong/gittest/baith.java
package com.company;

import java.util.Scanner;
import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class baith {
    public static void main(String[] args) {
        String s = "Hom Nay La Thu Ba AbC";
        String s1 = " toi di lam ";
        String s2 = " o cong ty ";
        int a = dem(s);
        System.out.println(" b1 : " + a);
        String y = loaibo(s);
        System.out.println(" b2 : " + y);
        String w = noichuoi(s1, s2);
        System.out.println(" b3 :" + w);
        String d = thaydoi(s);
        System.out.println(" b4 :" + d);
        String g = chuyendoi(s);
        System.out.println(" b5 :" + g);
        StringBuffer stringbf = new StringBuffer();

        Matcher m = Pattern.compile("([a-z])([a-z]*)",
                Pattern.CASE_INSENSITIVE).matcher(s);
        while (m.find()) {
            m.appendReplacement(stringbf,
                    m.group(1).toUpperCase() + m.group(2).toLowerCase());
        }
        System.out.println(" b6: " + m.appendTail(stringbf).toString());

        char[] sc = s.toCharArray();
        s = "";
        for (int i = 0; i < sc.length; i++) {
            int ascii = sc[i];

            if (ascii >= 65 && ascii <= 90) {
                s += (char) (ascii += 32);
            } else if (ascii >= 97 && ascii <= 122) {
                s += (char) (ascii -= 32);
            } else {
                s += (char) ascii;


            }
        }


        System.out.println(" b7 :" + s);
        {
            String p = Daochuoi(s);
            System.out.println(" b8 :" + p);

            int l = demchuoi(s1, s2);
            System.out.println(" b11 :" + l);
            String o = kiemtra(s1, s2);
            System.out.println(" b12 : " + o);
            String k1 = " nguyen van a ";
            String[] words = k1.split("\\s");


            String x = "";

            for (int i = 0; i < words.length; i++)
                if (i == words.length - 1)
                    System.out.println(words[i]);

                else
                    x = x + words[i];
            System.out.println(" 14:  " + x);

            Scanner input = new Scanner(System.in);
            System.out.println("18:  nhap chuoi :");
            String str = input.nextLine();
            System.out.println(" 18 :nhap ky tu can xoa ");
            String str2 = input.nextLine();
            String replaceString = str.replaceAll(str2, "");
            System.out.println("18 : " + replaceString);
            {
                String y1 = " ngon ngu lap trinh ";
                String[] word = y1.split("\\s");
                String z1 = " ";
                for (int i = word.length - 1; i >= 0; i--) {


                    z1 = z1 + word[i] + " ";

                }


                System.out.println(" 20 : " + z1);

            }
            {
                String k = new String ();
                Scanner nhap = new Scanner (System.in);
                System.out.println(" 23 : Nhap chuoi: ");
                s = nhap.nextLine();


                String replaceAll = s.replaceAll("nguoi", "");
                System.out.println("23 :" + replaceAll);
            }
        }



    }

    {
        String abc = "abc ad 123 456 789";


        abc = abc.replaceAll("[^0-9]", ",");


        String[] item = abc.split(",");


        for (int i = 0; i < abc.length(); i++) {


            try {
                Double.parseDouble(item[i]);
                System.out.println(" 17 : " + item[i]);
            } catch (NumberFormatException e) {
            }
        }

    }









    public static int dem(String s) {
        String replaceString = s.replaceAll(" ", "");
        return s.length() - replaceString.length();

    }

    public static String loaibo(String s) {
        String replaceString = s.replaceAll(" ", "");
        return replaceString;
    }

    public static String noichuoi(String s1, String s2) {
        String z = s1 + s2;
        return z;
    }

    public static String thaydoi(String s) {
        String x = s.toLowerCase();
        return s.toLowerCase();
    }

    public static String chuyendoi(String s) {
        String x = s.toUpperCase();
        return x;
    }

    public static String Daochuoi(String s) {
        String reverse = new StringBuffer(s).reverse().toString();
        return reverse;
    }

    public static int demchuoi(String s1, String s2) {
        String q = s1 + s2;
        int index = q.indexOf("cong");
        return index;
    }

    public static String kiemtra(String s1, String s2) {
        if (s1 == s2) {
            return "dung";
        }
        if (s1 != s2) {
            return "sai";
        }
        return " ";
    }


}

# MyRepository
