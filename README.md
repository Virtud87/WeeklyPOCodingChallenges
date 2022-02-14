# WeeklyPOCodingChallenges

# Week of Feb 14(Java)
public static String actualMemorySize(String memorySize) {

    double size = Double.parseDouble(memorySize.substring(0, memorySize.length() - 2));
    double actualSize = size * 0.93;

    if (memorySize.contains("MB")) {
      return String.valueOf(actualSize) + "MB";
    }
    if (memorySize.contains("GB") && (actualSize < 1)) {
        double sizeInMB = actualSize * 1024;
        return String.valueOf(sizeInMB) + "MB";
    }
    return String.valueOf(actualSize) + "GB";
  }
  
  # Week of Feb 14(Python)
  
  def atbash(sample_string):
  crypted = []
  for character in sample_string:
  
    if character.isalpha():
      ascii = ord(character)
      if 65 <= ascii <= 77:
        asciiCapitalFirstHalf = []
        count = 25
        amount_to_add = []
        for num in range(65, 78):
          asciiCapitalFirstHalf.append(num)
        for num in asciiCapitalFirstHalf:
          amount_to_add.append(count)
          count -= 2
        index = asciiCapitalFirstHalf.index(ascii)
        amount = amount_to_add[index]
        crypted.append(chr(ascii + amount))
      elif 78 <= ascii <= 90:
        asciiCapitalSecondHalf = []
        count = -1
        amount_to_add = []
        for num in range(78, 91):
          asciiCapitalSecondHalf.append(num)
        for num in asciiCapitalSecondHalf:
          amount_to_add.append(count)
          count -= 2
        index = asciiCapitalSecondHalf.index(ascii)
        amount = amount_to_add[index]
        crypted.append(chr(ascii + amount))
      elif 97 <= ascii <= 109:
        asciiLowerFirstHalf = []
        count = 25
        amount_to_add = []
        for num in range(97, 110):
          asciiLowerFirstHalf.append(num)
        for num in asciiLowerFirstHalf:
          amount_to_add.append(count)
          count -= 2
        index = asciiLowerFirstHalf.index(ascii)
        amount = amount_to_add[index]
        crypted.append(chr(ascii + amount))
      elif 110 <= ascii <= 122:
        asciiLowerSecondHalf = []
        count = -1
        amount_to_add = []
        for num in range(110, 123):
          asciiLowerSecondHalf.append(num)
        for num in asciiLowerSecondHalf:
          amount_to_add.append(count)
          count -= 2
        index = asciiLowerSecondHalf.index(ascii)
        amount = amount_to_add[index]
        crypted.append(chr(ascii + amount))
    else:
      crypted.append(character)   
  print("".join(crypted)) 
