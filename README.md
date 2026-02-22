# Maya-Calendar

</br>

![Compiler](https://github.com/user-attachments/assets/a916143d-3f1b-4e1f-b1e0-1067ef9e0401) ![10 Seattle](https://github.com/user-attachments/assets/c70b7f21-688a-4239-87c9-9a03a8ff25ab) ![10 1 Berlin](https://github.com/user-attachments/assets/bdcd48fc-9f09-4830-b82e-d38c20492362) ![10 2 Tokyo](https://github.com/user-attachments/assets/5bdb9f86-7f44-4f7e-aed2-dd08de170bd5) ![10 3 Rio](https://github.com/user-attachments/assets/e7d09817-54b6-4d71-a373-22ee179cd49c)  ![10 4 Sydney](https://github.com/user-attachments/assets/e75342ca-1e24-4a7e-8fe3-ce22f307d881) ![11 Alexandria](https://github.com/user-attachments/assets/64f150d0-286a-4edd-acab-9f77f92d68ad) ![12 Athens](https://github.com/user-attachments/assets/59700807-6abf-4e6d-9439-5dc70fc0ceca)  
![Components](https://github.com/user-attachments/assets/d6a7a7a4-f10e-4df1-9c4f-b4a1a8db7f0e) ![None](https://github.com/user-attachments/assets/30ebe930-c928-4aaf-a8e1-5f68ec1ff349)  
![Description](https://github.com/user-attachments/assets/dbf330e0-633c-4b31-a0ef-b1edb9ed5aa7) ![MayaCalendar](https://github.com/user-attachments/assets/db0798cc-5018-4e8b-8449-8a1f32ce468d)  
![Last Update](https://github.com/user-attachments/assets/e1d05f21-2a01-4ecf-94f3-b7bdff4d44dd) ![022026](https://github.com/user-attachments/assets/90c88085-69f5-4332-b090-2de107ca7f86)  
![License](https://github.com/user-attachments/assets/ff71a38b-8813-4a79-8774-09a2f3893b48) ![Freeware](https://github.com/user-attachments/assets/1fea2bbf-b296-4152-badd-e1cdae115c43)  

</br>

The Maya calendar is a system of calendars used in pre-Columbian Mesoamerica and in many modern communities in the Guatemalan highlands, [Veracruz](https://en.wikipedia.org/wiki/Veracruz), Oaxaca and [Chiapas](https://en.wikipedia.org/wiki/Chiapas), Mexico.

The essentials of the Maya calendar are based upon a system which had been in common use throughout the region, dating back to at least the 5th century BC. It shares many aspects with calendars employed by other earlier Mesoamerican civilizations, such as the Zapotec and Olmec and contemporary or later ones such as the [Mixtec](https://en.wikipedia.org/wiki/Mixtec_culture) and [Aztec calendars](https://en.wikipedia.org/wiki/Aztec_calendar).

</br>

![Main](https://github.com/user-attachments/assets/cc0b82ba-ef46-4dd2-9b15-a4fc06c21d01)

</br>

By the [Maya mythological](https://en.wikipedia.org/wiki/Maya_mythology) tradition, as documented in Colonial Yucatec accounts and reconstructed from Late Classic and Postclassic inscriptions, the deity [Itzamna](https://en.wikipedia.org/wiki/Itzamna) is frequently credited with bringing the knowledge of the calendrical system to the ancestral Maya, along with writing in general and other foundational aspects of Mayan culture.

</br>

# Tzolkʼin:  
The [tzolkʼin](https://en.wikipedia.org/wiki/Tzolk%CA%BCin) (in modern Maya orthography; also commonly written tzolkin) is the name commonly employed by Mayanist researchers for the Maya Sacred Round or 260-day calendar. The word tzolkʼin is a neologism coined in [Yucatec Maya](https://en.wikipedia.org/wiki/Yucatec_Maya_language), to mean "count of days" (Coe 1992). The various names of this calendar as used by precolumbian Maya people are still debated by scholars. The [Aztec](https://en.wikipedia.org/wiki/Aztecs) calendar equivalent was called [Tōnalpōhualli](https://en.wikipedia.org/wiki/T%C5%8Dnalp%C5%8Dhualli), in the Nahuatl language.

</br>

![signs](https://github.com/user-attachments/assets/abeb40e7-4cb9-49d6-b7df-58b32ce433f2)

</br>

The tzolkʼin calendar combines twenty day names with the thirteen day numbers to produce 260 unique days. It is used to determine the time of religious and ceremonial events and for divination. Each successive day is numbered from 1 up to 13 and then starting again at 1. Separately from this, every day is given a name in sequence from a list of 20 day

Complete Information : https://en.wikipedia.org/wiki/Maya_calendar

</br>

# Overview:  
The Maya calendar consists of several cycles or counts of different lengths. The 260-day count is known to scholars as the Tzolkin, or Tzolkʼin. The Tzolkin was combined with a 365-day vague solar year known as the [Haab](https://en.wikipedia.org/wiki/Haab%CA%BC) to form a synchronized cycle lasting for 52 Haabʼ called the Calendar Round. The Calendar Round is still in use by many groups in the Guatemalan highlands.

</br>

![Calendar](https://github.com/user-attachments/assets/bbd2688b-bfd4-493a-8f35-b9f9ce361fd7)

</br>

A different calendar was used to track longer periods of time and for the inscription of calendar dates (i.e., identifying when one event occurred in relation to others). This is the [Long Count](https://en.wikipedia.org/wiki/Mesoamerican_Long_Count_calendar). It is a count of days since a mythological starting-point. According to the correlation between the Long Count and Western calendars accepted by the great majority of Maya researchers (known as the Goodman-Martinez-Thompson, or GMT, correlation), this starting-point is equivalent to August 11, 3114 BC in the proleptic [Gregorian calendar](https://en.wikipedia.org/wiki/Proleptic_Gregorian_calendar) or September 6, in the [Julian calendar](https://en.wikipedia.org/wiki/Julian_calendar) (−3113 astronomical).

# Set Date:  
```pascal
procedure TForm1.bdatumClick(Sender: TObject);
  procedure kalende2(var ta,mo,ja:word);
  var
    sc:boolean;
  begin
      if ja<1 then ja:=1;
      if mo>13 then begin mo:=12 end;
      if mo<=0 then begin mo:=1 end;
      while ((ta>31) and (mo in [1,3,5,7,8,10,12])) or
            ((ta>30) and (mo in [4,6,9,11])) do dec(ta);
      if mo=2 then
      begin
        sc:=(ja mod 4=0);
        if (ja mod 100=0) and not(ja mod 400=0) then sc:=not sc;
        while sc and (ta>29) do dec(ta);
        while not sc and (ta>28) do dec(ta);
      end;
  end;
begin
    m_tag:=strtoint(edit3.text);
    m_monat:=strtoint(edit4.text);
    m_jahr:=strtoint(edit10.text);
    kalende2(m_tag,m_monat,m_jahr);
    edit3.text:=inttostr(m_tag);
    edit4.text:=inttostr(m_monat);
    edit10.text:=inttostr(m_jahr);

    superjd:=julian_date(encodedate(m_jahr,m_monat,m_tag));
    tzolkin_(superjd,m_z,m_n,m_h,m_p);
    m_hfest:=m_h;
    wi:=-(2*pi*(vv[(m_z-m_n+26) mod 13])+pi/10*(m_n));
    wialt:=wi;
    paintbox1paint(sender);
end;
```

</br>

# Calculate Tzolkʼin:  
```pascal
procedure tzolkin_(jd:extended;var z,n,h,p:integer);
var m:integer;
begin
    n:= trunc(jd) +136+1;
    m:= trunc(jd) + 65+1;
    z:= ((n - 1) mod 13) + 1;
    p:= m mod 365;
    h:= p mod 20;
    n:=n mod 20;
    p:=p div 20;
end;
````
