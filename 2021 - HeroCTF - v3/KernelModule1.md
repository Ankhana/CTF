# Kerner Module 1

#### So to begin we got this message :
```
Message from : Mom 23/04/21 21:00

Hey sweetheart !
I left a little something for you in the safe.
It's unlocked, so you just have to retrieve it.
Love you ! xoxo
PS : Happax, the cat, has been behaving oddly lately..

ssh -p 4822 kern1@ai.heroctf.fr
password : kern1_fip

Format : Hero{}

Author : iHuggsy
```

#### We then connect with the ssh information (I have voluntarily removed the superfluous information during the connection):

```console
$ ssh -p 4822 kern1@ai.heroctf.fr
kern1@ai.heroctf.fr's password: 
Welcome to Ubuntu 20.04.2 LTS (GNU/Linux 5.4.0-72-generic x86_64)
```

#### We launch the run file and we get this : 

```console
kern1@ns577466:~$ ./run

Welcome to the kernel challenge #1 !
---- Your share : host:/tmp/tmp.q3poiYccTF -> guest:/mnt/share ----
- Use CTRL+Z to put qemu in the background
- Use CTRL+* to exit the VM (shutdown)
- If qemu is in the background, use the 'fg' command to return to the vm


 **      **                           ******  ********** ********
/**     /**                          **////**/////**/// /**///// 
/**     /**  *****  ******  ******  **    //     /**    /**      
/********** **///**//**//* **////**/**           /**    /******* 
/**//////**/******* /** / /**   /**/**           /**    /**////  
/**     /**/**////  /**   /**   /**//**    **    /**    /**      
/**     /**//******/***   //******  //******     /**    /**      
//      //  ////// ///     //////    //////      //     //       

===============    Unlocked safe (by @iHuggsy)    ===============
=		      Kernel Challenge #1    		        =
=	     Can you read the flag from /dev/safe ?		=
=================================================================
```

#### We are asked to display the flag in /dev/safe
#### We move to /dev and test with **cat**. We get this:

```console
/dev $ cat safe
The cat goes :
"Meow, meow, MEOOOOOOW !"
```

#### It is easy to see that the cat command has been disabled to prevent us from reading the contents of the file. But the person didn't think to remove other commands like **more**. So we test with **more** :

```console
/dev $ more safe
Hero{s0_yOu_C4n_r34d_Fr0m_cHrD3v}
�p�LN�L�~���~���Kdflsu�
                       KX���d��M�x������dfluX���X������K0p��P�Ku�Kr�L�@@�/
```

#### We obtain the flag : Hero{s0_yOu_C4n_r34d_Fr0m_cHrD3v}