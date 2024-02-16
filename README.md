# CHALLENGE D: Use functions to optimize the SpongeBob theme!

use_bpm 136
use_synth :piano

define :the_song do
  #measure 13
  play :bb4
  sleep 0
  play :d5
  sleep 1
  play :bb4
  sleep 0
  play :d5
  sleep 0
  play :g5
  sleep 1
  play :bb4
  sleep 0
  play :d5
  sleep 0
  play :a5
  sleep 1
  play :bb4
  sleep 0
  play :d5
  sleep 0
  play :bb5
  sleep 1
end

live_loop:background_notes do
  play:E3, amp: 0.25
  sleep 1
  play:B3, amp: 0.25
  play:E4, amp: 0.25
  sleep 1
  play:B3, amp: 0.25
  sleep 1
  play:E4, amp: 0.25
  sleep 1
  
  
  play:E3, amp: 0.5
  sleep 1
  play:B3, amp: 0.5
  play:E4, amp: 0.5
  sleep 1
  play:B3, amp: 0.5
  sleep 1
  play:E4, amp: 0.5
  sleep 1
  
  
  play:E3, amp: 0.75
  sleep 1
  play:B3, amp: 0.75
  play:E4, amp: 0.75
  sleep 1
  play:B3, amp: 0.75
  sleep 1
  play:E4, amp: 0.75
  sleep 1
  
  
  5.times do
    play:E3, amp: 1
    sleep 1
    play:B3, amp: 1
    play:E4, amp: 1
    sleep 1
    play:B3, amp: 1
    sleep 1
    play:E4, amp: 1
    sleep 1
  end
  play :c2, sustain: 3
  play :e2, sustain: 4
  play :g2, sustain: 2
  play :b2, sustain: 2
  stop
end

live_loop:this_loop do
  7.times do
    the_song
  end
  stop
end

live_loop:that_loop do
  30 nm.times do
    sample :drum_snare_soft
    sleep 1
  end
  stop
end
define :the_first do
  play:E4
  sleep 1
  play:E5
  play:Gs4
  sleep 2
  play:E5
  play:Gs4
  sleep 1
end

define :the_second do
  play:B4
  sleep 0.75
  play:As4
  sleep 0.25
  play:Gs4
  play:B4
  sleep 0.75
  play:Cs5
  sleep 0.25
  play:B4
  sleep 1
  play:Gs4
  play:E5
  sleep 1
end

define :the_third do
  play :r
  sleep 1
  play:E5
  play:Gs4
  play:B4
  sleep 1
  play:B4
  sleep 1
  play:E5
  play:Gs4
  sleep 1
  end
  
  # Measure 1
  play :r
  sleep 1
  play:E4
  play:Gs4
  sleep 2
  play:E5
  play:Gs4
  sleep 1
  
  # Measure 2
  the_first
  
  # Measure 3
  the_third
  
  # Measure 4
  the_third
  
  # Measure 5
  the_second
  
  # Measure 6
  the_third
  
  # Measure 7
  the_second
  
  # Measure 8
  the_first
