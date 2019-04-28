# DateandTime
For ico to check the start date and end time and to check whether the ico is running or closed
pragma solidity >=0.4.2;

contract DateandTime{
    uint public startTime;
    uint public endTime;
    constructor() public{
        startTime = now;
        
    }
    function setTime(uint start,uint end) public {
        startTime = start;
        endTime = end;
    }
    function getDate() public view returns(uint){
        return now;
    }
    function isClosed() public view returns(bool){
        if(startTime < now)
        {
            return false;
        }
        else{
            return true;
        }
    }
}
