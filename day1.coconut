with open('./inputs/day1.txt') as infile:
  lines = list(map(int, infile.readlines()))

prev = None
increases = 0
for line in lines:
  if prev is not None and line > prev:
    increases += 1
  prev = line

print(f'part 1 = {increases}')
# end part 1

pt = 0
sliding_sum = 0
increases = 0
while pt < 3:
  sliding_sum += lines[pt]
  pt += 1

while pt < len(lines):
  new_sliding_sum = sliding_sum - lines[pt-3] + lines[pt]
  if new_sliding_sum > sliding_sum:
    increases += 1
  sliding_sum = new_sliding_sum
  pt += 1

print(f'part 2 = {increases}')
