# utl-solving-the-Josephus-problem-in-each-of-seventy-four-languages
Solving the Josephus problem in each of seventy-four languages  

    Solving the Josephus problem in each of seventy-four languages                                                      
                                                                                                                        
    R solution provides.                                                                                                
                                                                                                                        
    If you have IML/R just paste the code below or                                                                      
    use my interface.                                                                                                   
                                                                                                                        
    github                                                                                                              
    https://tinyurl.com/y5z2uch5                                                                                        
    https://github.com/rogerjdeangelis/utl-solving-the-Josephus-problem-in-each-of-seventy-four-languages               
                                                                                                                        
    SAS Forum                                                                                                           
    https://communities.sas.com/t5/New-SAS-User/Josephus-problem/m-p/570601                                             
                                                                                                                        
    74 solutions                                                                                                        
    https://rosettacode.org/wiki/Josephus_problem#R                                                                     
                                                                                                                        
    macros                                                                                                              
    https://tinyurl.com/y9nfugth                                                                                        
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories                          
                                                                                                                        
    Josephus problem is a math puzzle with a grim description: n                                                        
    prisoners are standing on a circle, sequentially numbered from                                                      
     0 to  n .                                                                                                          
                                                                                                                        
    An executioner walks along the circle, starting from prisoner 0 ,                                                   
    removing every  k-th prisoner and killing him.                                                                      
                                                                                                                        
    As the process goes on, the circle becomes smaller and smaller,                                                     
    until only one prisoner remains, who is then freed.                                                                 
                                                                                                                        
    For example, if there are  n=5 prisoners and  k=2 ,                                                                 
    the order the prisoners are killed in                                                                               
    (let's call it the "killing sequence")                                                                              
    will be 1, 3, 0, and 4, and the survivor will be #2.                                                                
                                                                                                                        
    Given any  n,k>0 ,   find out which prisoner will be the final survivor.                                            
                                                                                                                        
    In one such incident, there were 41 prisoners and every                                                             
    3rd prisonerwas being killed  k=3.                                                                                  
                                                                                                                        
    Among them was a clever chap name Josephus who worked out the problem,                                              
    stood at the surviving position, and lived on to tell the tale.                                                     
                                                                                                                        
    Which number was he?                                                                                                
                                                                                                                        
    *_                   _                                                                                              
    (_)_ __  _ __  _   _| |_                                                                                            
    | | '_ \| '_ \| | | | __|                                                                                           
    | | | | | |_) | |_| | |_                                                                                            
    |_|_| |_| .__/ \__,_|\__|                                                                                           
            |_|                                                                                                         
    ;                                                                                                                   
                                                                                                                        
             41 Prisoners arraged in a Circle                                                                           
               Kill every third prisoner                                                                                
                and shrink circle                                                                                       
           who is the final standing prisoner                                                                           
                                                                                                                        
                                                                                                                        
                   ************                                                                                         
                ****          ***                                                                                       
              ***                **                                                                                     
         39 ***                   ***                                                                                   
           **                       **                                                                                  
       40  *                         **                                                                                 
          **                          *                                                                                 
      41 **             O             **                                                                                
         *            --|              *                                                                                
      0 *              / \             *                                                                                
        *                              *                                                                                
       1 *                             *                                                                                
         *                             *                                                                                
        2**                           **                                                                                
          **                          *                                                                                 
         3 *                         **                                                                                 
           **                        **                                                                                 
          4 ***                   ***                                                                                   
              ***                **                                                                                     
             5  ****          ***                                                                                       
                   ************                                                                                         
                                                                                                                        
    *            _               _                                                                                      
      ___  _   _| |_ _ __  _   _| |_                                                                                    
     / _ \| | | | __| '_ \| | | | __|                                                                                   
    | (_) | |_| | |_| |_) | |_| | |_                                                                                    
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                                   
                    |_|                                                                                                 
    ;                                                                                                                   
                                                                                                                        
    The lucky prisoner is #30 in the original sequence                                                                  
                                                                                                                        
    [1] 30                                                                                                              
                                                                                                                        
    *____              _       _   _                                                                                    
    |  _ \   ___  ___ | |_   _| |_(_) ___  _ __                                                                         
    | |_) | / __|/ _ \| | | | | __| |/ _ \| '_ \                                                                        
    |  _ <  \__ \ (_) | | |_| | |_| | (_) | | | |                                                                       
    |_| \_\ |___/\___/|_|\__,_|\__|_|\___/|_| |_|                                                                       
                                                                                                                        
    ;                                                                                                                   
                                                                                                                        
                                                                                                                        
    r is the number of remained prisoner.                                                                               
                                                                                                                        
    (0.2.3.4.5.6.7,...40                                                                                                
                                                                                                                        
    %utl_submit_r64('                                                                                                   
     jose <-function(s,r,n){                                                                                            
      y <- 0:(r-1);                                                                                                     
      for (i in (r+1):n)                                                                                                
        y <- (y + s) %% i;                                                                                              
        return(y);                                                                                                      
      };                                                                                                                
    jose(3,1,41);                                                                                                       
    ');                                                                                                                 
                                                                                                                        
    [1] 30                                                                                                              
                                                                                                                        
