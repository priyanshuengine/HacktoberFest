def binary_search(ml, elem):
   low = 0
   high = len(ml) - 1
   mid = 0
   while low <= high:
      mid = (high + low) // 2
      if ml[mid] < elem:
         low = mid + 1
      elif ml[mid] > elem:
         high = mid - 1
      else:
         return mid
   return -1

my_list = [ 1, 9, 11, 21, 34, 54, 67, 90 ]
elem_to_search = 1
print("The list is")
print(ml)

my_result = binary_search(ml, elem_to_search)

if my_result != -1:
   print("Element found at index ", str(my_result))
else:
   print("Element not found!")
