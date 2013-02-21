Racer
=====


def roll_dice
  dice = rand(6) + 1
end

def track
  track_a = Array.new(25) { "" }
  track_b = Array.new(25) { "" }
  track_a[0] = "a"
  track_b[0] = "b"
  #starting position
  counter_a = 0
  counter_b = 0

  #roll dice to determine next spot

  while counter_a < 25 || counter_b < 25
    track_a[counter_a] = ""
    track_b[counter_b] = ""

    counter_a += roll_dice
    counter_b += roll_dice
    if counter_a > 25 || counter_b > 25
      puts "game over"
      exit
    end
    track_a[counter_a] = "a"
    track_b[counter_b] = "b"
  

    track_a.each do |track| 
      print track + " | "
    end
    puts "" 
    track_b.each do |track| 
      print track + " | "
    end
    puts ""
  end

end

track

#def print_track(array)
