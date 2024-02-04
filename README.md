# class-for-a-digital-clock

class DigitalClock {
  int _hours = 0;
  int _minutes = 0;
  int _seconds = 0;

  // Method to set the time
  void setTime(int hours, int minutes, int seconds) {
    if (hours >= 0 && hours < 24 && minutes >= 0 && minutes < 60 && seconds >= 0 && seconds < 60) {
      _hours = hours;
      _minutes = minutes;
      _seconds = seconds;
    } else {
      print("Invalid time values");
    }
  }

  // Method to display the time
  void displayTime() {
    print("Time: ${_formatTime(_hours)}:${_formatTime(_minutes)}:${_formatTime(_seconds)}");
  }

  // Private method to format time with leading zeros
  String _formatTime(int time) {
    return time < 10 ? '0$time' : '$time';
  }
}

void main() {
  // Example usage
  DigitalClock myClock = DigitalClock();
  myClock.setTime(04, 13, 40);
  myClock.displayTime();
}
