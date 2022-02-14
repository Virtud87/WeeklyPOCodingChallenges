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
