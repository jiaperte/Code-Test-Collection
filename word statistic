//Java 8 word statistic 
//How to sort map by value ascending or descending
//How to print value and key in a map

public static void staticStr(String str) {
  Map<String, Integer> hp = new HashMap<>();
  String[] words;
  words = str.split(" ");
  for(String  word : words) {
    if(!hp.containsKey(word)) {
      hp.put(word, 1);
      continue;
    }
    hp.put(word, hp.getOrDefault(word, 0)+1);
  }
  
  Map<String, Integer> sorted = new HashMap<>();
  sorted = hp
          .entrySet()
          .stream()
          .sorted(Collections.reverseOrder(Map.Entry.comparingByValue()))
          //descending
          //.sorted(comparingByValue()) asending
          .collect(
              toMap(Map.Entry::getKey, Map.Entry::getValue, (e1, e2) -> e2,
                  LinkedHashMap::new));

  sorted.entrySet().forEach(entry->{
  System.out.println(entry.getKey() + " " + entry.getValue());
  });
}
